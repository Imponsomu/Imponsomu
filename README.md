





- 👋 Hi, I’m @Imponsomu
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Imponsomu/Imponsomu is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->



message FrameActionBody {
  bytes frame_url = 1;      // The URL of the frame app
  bytes button_index = 2;   // The index of the button that was clicked
  CastId cast_id = 3;       // The cast which contained the frame URĽ
  bytes input_text = 4;     // The text from the user input (if any)
  bytes state = 5;          // Serialized frame state value
  bytes transaction_id = 6; // Transaction ID
  bytes address = 7;        // User's connected address
}

// MessageType and MessageData are extended to support the FrameAction

enum MessageType {
  .....
  MESSAGE_TYPE_FRAME_ACTION = 13;
}

message MessageData {
  oneof body {
		...
		FrameActionBody frame_action_body = 16
  }
}






