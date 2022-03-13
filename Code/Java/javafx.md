# JavaFX

## Installation

### Maven Dependency

org.openjfx:javafx-fxml:16

### PATH_TO_FX

/Library/Java/JavaVirtualMachines/javafx-sdk-17.0.1/lib

### VM-Options

--module-path /Library/Java/JavaVirtualMachines/javafx-sdk-17.0.1/lib --add-modules javafx.controls,javafx.fxml



## Startup

```java
  @Override
    public void start(Stage primaryStage) throws Exception{
        Parent root = FXMLLoader.load(getClass().getResource("login.fxml"));
        Scene scene = new Scene(root);
        primaryStage.setTitle("Digitaler Speiseplan");
        primaryStage.setScene(scene);
        primaryStage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
```

## Communication between scenes

```java
public void switchToSceneMenu (ActionEvent event) throws IOException {

        FXMLLoader loader;
        loader = new FXMLLoader(getClass().getResource("menu.fxml"));
        root = loader.load();

        MenuController menuController = loader.getController();

        // setRole in menuControler 
        menuController.setRole(role);

        stage = (Stage) ((Node) event.getSource()).getScene().getWindow();
        scene = new Scene(root);
        stage.setScene(scene);
        stage.show();
    }
```