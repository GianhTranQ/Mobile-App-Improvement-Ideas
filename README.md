# Mobile App Improvement - Ideas:

## Application Architecture: MVVM (Model-View-ViewModel)
<img src="https://github.com/GianhTranQ/Mobile-App-Improvement-Ideas/blob/main/mad-arch-overview.png" width="500">

Application should have at least two layers
- The UI layer that displays application data on the screen (View and ViewModel)
- The data layer that contains the business logic of your app and exposes application data (Model)

We can add an additional layer called the domain layer to simplify and reuse the interactions between the UI and data layers.

Here are benefits of MVVM

- Business logic is decoupled from UI
- Easy to maintain and test
- Easy to reuse components
- Loosely coupled architecture: MVVM makes our application architecture as loosely coupled.
- We can write unit test cases for both the viewmodel and Model layer without the need to reference the View.

### UI layer: View - ViewModel: 
<img src="https://github.com/GianhTranQ/Mobile-App-Improvement-Ideas/blob/main/mad-arch-overview-ui.png" width="500">

The role of the UI layer (or presentation layer) is to display the application data on the screen. Whenever the data changes, either due to user interaction (such as pressing a button) or external input (such as a network response), the UI should update to reflect the changes.
The UI layer is made up of two thing:

- View: UI elements that render the data on the screen
- ViewModel: State holders - that hold data, expose it to the UI, and handle logic

### Data layer: Model
<img src="https://github.com/GianhTranQ/Mobile-App-Improvement-Ideas/blob/main/mad-arch-overview-data.png" width="500">

The data layer of an app contains the business logic. The business logic is what gives value to our app—it's made of rules that determine how our app creates, stores, and changes data.

The data layer is made of repositories that each can contain zero to many data sources


## Technical advice
- Strong type language: migrate to Type Script (TypeScript is a language which extends JavaScript by adding type definitions, much like Flow. While React Native is built in Flow, it supports both TypeScript and Flow by default) refer [here](https://reactnative.dev/blog/2018/05/07/using-typescript-with-react-native)
- Apply Repository pattern for Data layer
- Use a state container like Redux for UI later
