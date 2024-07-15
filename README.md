# Evaluation_Submission_Annie_Sneha
Evaluation Submission
const { defineConfig } = require("cypress");
const cucumber = require('cypress-cucumber-preprocessor').default;


async function setupNodeEvents(on,config){
  on('file:preprocessor', cucumber())
  return config;
}

module.exports = defineConfig({
  e2e: {
    setupNodeEvents,
    specPattern: 'cypress/integration/Evaluation/*.js' 
    //Form.feature
  },
});

