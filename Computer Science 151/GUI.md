---
tags:
  - cs151
---
## JFrame

### Five steps to displaying a frame
1. `JFrame frame = new JFrame();`
2. `frame.setSize(300,400);`
3. `frame.setTitle("An Empty Frame");`
4. `frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);`
5. `frame.setVisible(true);`

*Don't forget to import javax.swing.JFrame*
### Adding Components

* You cannot directly add to the JFrame
* Instead, construct an object and add it to the frame
	* Examples
		* JComponent
		* JPanel
		* JTextComponent
		* JLabel
```java
// Extend the JComponent Class
public class RectangleComponent extends JComponent {

	// Override JComponent's paintComponent method
	@Override
	public void paintComponent(Graphics g) {
		// Drawing instructions go here
	}
}
```
### Adding Panels

* Add components into a panel (a container for other UI components) and then add the panel to the frame
```java
JButton button = new JButton("Click me");
JPanel panel new JPanel();
panel.add(button);
```

### Using inheritance to customize frames

* For complex frames
	* Design a subclass of `JFrame`
	* Store the components as instance variables
	* Initialize them in the constructor of your variables
```java
public class FilledFrame extends JFrame {
	private JButton button;
	private JLabel label;
	private static final int FRAME_WIDTH = 400;
	private static final int FRAME_HEIGHT = 300;

	private void createComponents() {
		button = new JButton("Click me");
		label = new JLabel("Hello world");
		JPanel = new JPanel();
		panel.add(button);
		panel.add(label);
		add(panel);
	}
}

public class FilledFrameViewer {
	public static void main(String[] args) {
		JFrame frame = new FilledFrame();
		frame.setTitle("A frame");
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.setVisible(true);
	}
}
```
>[!tip]
>You can add the main method directly to the class(FilledFrame in this case)
## Events and Event Handling

* In a modern GUI program, the user controls the program through the mouse and keyboard
* The user can perform actions via mouse and keyboard, and the program can be set up to receive and handle inputs from the mouse and keyboard

### Action Listener

```java
// The ActionListener interface has one method
public interface ActionListener {
	void actionPerformed(ActionEven event);
}

import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

public class ClickListener implements ActionListener {

	public void actionPerformed(ActionEvent event) {
		System.out.println("I was clicked");
	}
}
```

#### Registering the Action Listener

A `ClickListener` object must be created, and then registered to a specific event source
```java
ActionListener listener = new ClickListener();
button.addActionListener(listener);
// When the button object is clicked, it will call listener.ActionPerformed, passing it the event as a parameter
```

>[!warning]
>Add the `ActionListener` after adding the components to the panel and adding the panel to frame



