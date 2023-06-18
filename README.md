# Introduction

This repository contains EEBUS message responses from EEBUS compatible devices highlighting their capabilities.

The relevant messages are response for `NodeManagementDetailedDiscoveryData` and `NodeManagementUseCaseData` calls. The [Enbility devices](https://enbility.net/devices/) website summarizes the details.

## Contribution

To add more data, feel free to create a PR with the corresponding messages. Please also update or add the corresponding data into the `devices.json` file as part of the PR.

The data can be collected by using the [eebus-go](https://github.com/enbility/eebus-go/) library and follow its usage details. It does not matter if the EVSE or HEMS variant is used.

## Structure

- Each brand will get its own folder
- Each device/service gets its own subfolder under the brand
- Each folder contains:
  - `discovery-data.json` for the `NodeManagementDetailedDiscoveryData` response
  - `usecase-data.json` for the `NodeManagementUseCaseData` response
  - `device.json` for the summary & findings for each device/service
- The root folders `device.json` contains a list of relative paths to the `device.json` files
- The root folders `usecases.json` file contains details about each known use case
- The root folder `schema` contains JSON schema for all the different json files
- The repository contains a default setting for VS Code to automatically use the JSON schema files when editing the various JSON files

## Todo / Wishlist

- Automatically create a generic `device.json` file for provided SPINE responses
