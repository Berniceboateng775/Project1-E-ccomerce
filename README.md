# Project1-E-ccomerce
Developed a web-based multi-vendor platform where sellers can list their products, and users can search for items and place orders. The system will be designed using a microservices architecture, breaking down the platform into modular, independent services such as authentication, product management, order processing, and notifications.

<h1 align="center"> Ecommerce Microservice </h1> <br>

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Requirements](#requirements)
- [Quickstart](#quick-start)
- [API](#documentation)

## Introduction

This project is an Ecommerce web application with its backend architecture implemented in a microservice pattern with a monolithic frontend.

## Features
Here are some of the features:

- User authentication
- Users can make payment in a seamless manner
- Uses JWT (Json Web Tokens) for Authorization Tokens
- Add products to the cart seamlessly
- Built using well-established tools - Node, GraphQL, JWT, React
- Users can complete an order within seconds

## Tech Stack
- Node
- GraphQL
- Docker
- Kafka
- Zookeeper
- React

## Quick Start

The goal of this quick start is to get a working application quickly up and running. To start a dockerized version of the ecommerce microservice, you can do the following:

1. Change directory into the api-gateway and run:
   ```bash
   docker-compose up -d
