<script setup lang="ts">
import { ref } from 'vue'

const url = ref('https://techdebt-slides.netlify.app')
const testPrompts = ref('Check if the homepage loads successfully\nVerify the navigation menu is visible\nConfirm the search bar is functional')
</script>

<template>
  <div style="all: revert; font-family: Times, serif; font-size: 16px; color: black; background: white; margin: 0; padding: 10px; border: 4px outset #c0c0c0; background: #f0f0f0;">
    <div style="all: revert; margin: 8px 0;">
      <label style="all: revert; font-family: Times, serif; font-size: 16px; color: black;">URL:</label>
      <input
        type="url"
        v-model="url"
        placeholder="Enter website URL"
        style="all: revert; font-family: Times, serif; font-size: 16px; border: 2px inset; padding: 1px 2px; margin-left: 4px; width: 300px;"
      >
      <button style="all: revert; font-family: Times, serif; font-size: 16px; border: 2px outset; background: ButtonFace; padding: 2px 6px; margin-left: 4px;">Load Site</button>
    </div>

    <table
      width="100%"
      style="all: revert; border-collapse: separate; border-spacing: 2px; margin-top: 16px; width: 100%;"
    >
      <tr style="all: revert; width: 100%;">
        <td width="100%" style="all: revert; vertical-align: top; padding-right: 8px;">
          <div style="all: revert; width: 100%;">
            <label style="all: revert; font-family: Times, serif; font-size: 16px; color: black;">AI Test Prompts (Natural Language):</label>
            <br style="all: revert;">
            <textarea
              v-model="testPrompts"
              rows="20"
              cols="35"
              placeholder="Write your tests in natural language..."
              style="all: revert; font-family: monospace; font-size: 13px; border: 2px inset; padding: 2px; margin-top: 4px; resize: both; width: 100%; box-sizing: border-box;"
            ></textarea>
          </div>
        </td>
        <td width="100%" style="all: revert; vertical-align: top; padding-left: 8px;">
          <div style="all: revert;">
            <label style="all: revert; font-family: Times, serif; font-size: 16px; color: black;">Website Preview:</label>
            <br style="all: revert;">
            <iframe
              :src="url"
              width="100%"
              height="800"
              frameborder="1"
              style="all: revert; border: 2px inset; margin-top: 4px; width: 100%; box-sizing: border-box; height: 290px;"
            ></iframe>
          </div>
        </td>
      </tr>
    </table>
  </div>
</template>