# reactNativeExpoApp
how to make React Native app with expo typescript and tailwind(nativewind)

## Creating a new project

### Install globaly the CLI:
    npm i -g expo-cli
### Create a project: 
	npx create-expo-app -t expo-template-blank-typescript
### cd into the project
## Add tailwind(nativewind)
 npm i nativewind
 npm i --dev tailwindcss
 npx tailwindcss init
### 	then change babel.config.js(customize based on your directory
		- content: [],
		+ content: ["./App.{js,jsx,ts,tsx}", "./<custom directory>/**/*.{js,jsx,ts,tsx}"],
### add babel plugin
 		+   plugins: ["nativewind/babel"],
	
### add this line to src/tailwindcss-react-native.d.ts
		/// <reference types="nativewind/types" />
### Done🙂🙂,now you can use without errors
		<View className="flex-1 items-center justify-center bg-white"> 		

## Adding TypeScript to existing projects

    Create a blank TypeScript config: touch tsconfig.json
    Run yarn start or npm run start to automatically configure TypeScript
    Rename files to TypeScript, .tsx for React components and .ts for plain typescript files

    bulb You can disable the TypeScript setup in Expo CLI with the environment variable EXPO_NO_TYPESCRIPT_SETUP=1 expo start
