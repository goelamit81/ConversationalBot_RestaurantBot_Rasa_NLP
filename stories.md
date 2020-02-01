<!-- markdownlint-disable -->

<!-- greet, one after another, location first -->

## interactive_story_01_greet_ask_location_valid_ask_cuisine_valid_ask_budget_ask_email_with_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_02_greet_ask_location_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_03_greet_location_valid_ask_cuisine_valid_ask_budget_ask_email_with_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_04_greet_location_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_05_greet_ask_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_with_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location
  - action_slot_reset
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_06_greet_ask_location_invalid_retry_without_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_with_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
  - action_slot_reset
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine  
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_07_greet_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_with_affirm_send_email_without_thank
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_08_greet_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_09_greet_ask_location_out_of_scope_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_with_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* out_of_scope
  - action_slot_reset
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_10_greet_ask_location_out_of_scope_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* out_of_scope
  - action_slot_reset
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_11_greet_location_invalid_retry_without_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bye
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_bye
  - action_restart

## interactive_story_12_greet_location_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bye
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_bye
  - action_restart

## interactive_story_13_greet_location_invalid_retry_without_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_without_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_14_greet_location_valid_ask_cuisine_valid_ask_budget_ask_email_without_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_15_greet_ask_location_valid_ask_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_with_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_16_greet_ask_location_valid_ask_cuisine_invalid_retry_without_affirm_valid_ask_budget_ask_email_with_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

<!-- no greet, one after another, location first -->

## interactive_story_17_no_greet_location_valid_ask_cuisine_valid_ask_budget_ask_email_with_affirm_send_email_bye
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_18_no_greet_location_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_19_no_greet_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_with_affirm_send_email_thank
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_20_no_greet_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_21_no_greet_location_invalid_retry_without_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bye
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_bye
  - action_restart

## interactive_story_22_no_greet_location_invalid_retry_without_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_without_affirm_send_email_thank
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_23_no_greet_location_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bye
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_bye
  - action_restart

## interactive_story_24_no_greet_location_valid_ask_cuisine_valid_ask_budget_ask_email_without_affirm_send_email_bye
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_25_no_greet_ask_location_valid_ask_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_with_affirm_send_email_thank
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_26_no_greet_ask_location_valid_ask_cuisine_invalid_retry_without_affirm_valid_ask_budget_ask_email_with_affirm_send_email_thank
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_27_no_greet_location_valid_ask_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_with_affirm_send_email_thank
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_28_no_greet_location_valid_ask_cuisine_invalid_retry_without_affirm_valid_ask_budget_ask_email_with_affirm_send_email_thank
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_29_no_greet_location_valid_ask_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_with_affirm_send_email_bye
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_30_no_greet_location_valid_ask_cuisine_invalid_retry_without_affirm_valid_ask_budget_ask_email_with_affirm_send_email_bye
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_31_no_greet_location_valid_ask_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_without_affirm_send_email_bye
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_32_no_greet_location_valid_ask_cuisine_invalid_retry_without_affirm_valid_ask_budget_ask_email_without_affirm_send_email_bye
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

<!-- greet, one after another, cuisine first -->

## interactive_story_33_greet_cuisine_valid_ask_location_valid_ask_budget_ask_email_with_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_34_greet_cuisine_valid_ask_location_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_35_greet_cuisine_invalid_retry_with_affirm_valid_ask_location_valid_ask_budget_ask_email_with_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_36_greet_cuisine_invalid_retry_with_affirm_valid_ask_location_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_37_greet_cuisine_valid_location_invalid_retry_without_affirm_valid_then_budget_followed_by_email
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_38_greet_cuisine_valid_ask_location_invalid_retry_with_affirm_valid_ask_budget_ask_email_with_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_39_greet_cuisine_valid_location_invalid_retry_with_affirm_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_40_greet_cuisine_valid_ask_location_valid_ask_budget_ask_email_with_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_41_greet_cuisine_valid_ask_location_valid_ask_budget_ask_email_without_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_42_greet_cuisine_invalid_retry_with_affirm_valid_ask_location_valid_ask_budget_ask_email_without_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_43_greet_cuisine_invalid_retry_with_affirm_valid_ask_location_valid_ask_budget_ask_email_without_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_44_greet_cuisine_invalid_retry_without_affirm_valid_ask_location_valid_ask_budget_ask_email_without_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_45_greet_cuisine_invalid_retry_without_affirm_valid_ask_location_valid_ask_budget_ask_email_without_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_46_greet_cuisine_valid_ask_location_invalid_retry_without_affirm_valid_ask_budget_ask_email_deny_email_bye
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_bye
  - action_restart

<!-- no greet, one after another, cuisine first -->

## interactive_story_47_no_greet_cuisine_valid_ask_location_valid_ask_budget_ask_email_with_affirm_send_email_bye
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_48_no_greet_cuisine_valid_ask_location_valid_ask_budget_ask_email_with_affirm_send_email_thank
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_49_no_greet_cuisine_valid_ask_location_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_50_no_greet_cuisine_invalid_retry_with_affirm_valid_ask_location_valid_ask_budget_ask_email_with_affirm_send_email_bye
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_51_no_greet_cuisine_invalid_retry_without_affirm_valid_ask_location_valid_ask_budget_ask_email_with_affirm_send_email_bye
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_52_no_greet_cuisine_invalid_retry_with_affirm_valid_ask_location_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_53_no_greet_cuisine_invalid_retry_without_affirm_valid_ask_location_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_54_no_greet_cuisine_valid_ask_location_invalid_retry_with_affirm_valid_ask_budget_ask_email_with_affirm_send_email_bye
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_55_no_greet_cuisine_valid_ask_location_invalid_retry_with_affirm_valid_ask_budget_ask_email_with_affirm_send_email_thank
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_56_no_greet_cuisine_valid_ask_location_invalid_retry_with_affirm_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_57_no_greet_cuisine_valid_ask_location_invalid_retry_without_affirm_valid_ask_budget_ask_email_without_affirm_send_email_bye
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_58_no_greet_cuisine_valid_ask_location_invalid_retry_without_affirm_valid_ask_budget_ask_email_without_affirm_send_email_thank
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

<!-- greet, location + cuisine-->

## interactive_story_59_greet_location_and_cuisine_together_valid_ask_budget_ask_email_with_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant{"location": "Mumbai", "cuisine": "chinese"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_60_greet_location_and_cuisine_together_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant{"location": "agra", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_61_greet_location_and_cuisine_together_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_send_email_thank
* greet
  - utter_greet
* search_restaurant{"location": "Mumbai", "cuisine": "chinese"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_62_greet_location_and_cuisine_together_cuisine_invalid_retry_without_affirm_valid_ask_budget_ask_email_send_email_thank
* greet
  - utter_greet
* search_restaurant{"location": "Mumbai", "cuisine": "chinese"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_63_greet_location_and_cuisine_together_cuisine_invalid_retry_without_affirm_valid_ask_budget_ask_email_send_email_bye
* greet
  - utter_greet
* search_restaurant{"location": "Mumbai", "cuisine": "chinese"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_64_greet_location_and_cuisine_together_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant{"location": "agra", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_65_greet_location_and_cuisine_together_cuisine_invalid_retry_without_affirm_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant{"location": "agra", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_66_greet_location_and_cuisine_together_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_with_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"location": "agra", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_67_greet_location_and_cuisine_together_cuisine_invalid_retry_without_affirm_valid_ask_budget_ask_email_with_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"location": "agra", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_68_greet_location_and_cuisine_together_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_with_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"location": "Delhi", "cuisine": "french"}
  - action_location_valid
  - slot{"location_validity": "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location
* search_restaurant{"location": "Delhi"}
  - action_location_valid
  - slot{"location_validity": "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "french"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity": "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_69_greet_location_and_cuisine_together_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant{"location": "Vizag", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location
* search_restaurant{"location": "Vizag"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "italian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_70_greet_location_and_cuisine_together_location_invalid_retry_without_affirm_valid_ask_budget_ask_email_with_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"location": "agra", "cuisine": "italian"} 
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "agra"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_71_greet_location_and_cuisine_together_location_invalid_retry_without_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* greet
  - utter_greet
* search_restaurant{"location": "Vizag", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
  - action_slot_reset
* search_restaurant{"location": "Vizag"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "italian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_72_greet_location_and_cuisine_together_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_without_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"location": "Delhi", "cuisine": "french"}
  - action_location_valid
  - slot{"location_validity": "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location
* search_restaurant{"location": "Delhi"}
  - action_location_valid
  - slot{"location_validity": "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "french"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity": "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_73_greet_location_and_cuisine_together_location_invalid_retry_without_affirm_valid_ask_budget_ask_email_without_affirm_send_email_bye
* greet
  - utter_greet
* search_restaurant{"location": "agra", "cuisine": "italian"} 
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "agra"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

<!-- no greet, location + cuisine -->

## interactive_story_74_no_greet_location_and_cuisine_together_valid_ask_budget_ask_email_with_affirm_send_email_thank
* search_restaurant{"cuisine":"indian","location":"Mysore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget":"high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_75_no_greet_location_and_cuisine_together_valid_ask_budget_ask_email_deny_email_bye
* search_restaurant{"cuisine":"indian","location":"Mysore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget":"high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_bye
  - action_restart

## interactive_story_76_no_greet_location_and_cuisine_together_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_with_affirm_send_email_bye
* search_restaurant{"cuisine":"indian","location":"Mysore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget":"high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_77_no_greet_location_and_cuisine_together_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_deny_email_bye
* search_restaurant{"cuisine":"indian","location":"Mysore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget":"high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_bye
  - action_restart

## interactive_story_78_no_greet_location_and_cuisine_together_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_with_affirm_send_email_bye
* search_restaurant{"location": "agra", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_79_no_greet_location_and_cuisine_together_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_with_affirm_send_email_bye
* search_restaurant{"location": "Delhi", "cuisine": "french"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location
* search_restaurant{"location": "Delhi"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "french"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_80_no_greet_location_and_cuisine_together_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_bot_helpful_with_affirm
* search_restaurant{"location": "Vizag", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location
* search_restaurant{"location": "Vizag"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "italian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* affirm
  - utter_happy
  - utter_bye
  - action_restart

## interactive_story_81_no_greet_location_and_cuisine_together_location_invalid_retry_without_affirm_valid_ask_budget_ask_email_with_affirm_send_email_bye
* search_restaurant{"location": "agra", "cuisine": "italian"} 
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "agra"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_82_no_greet_location_and_cuisine_together_location_invalid_retry_without_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_without_affirm_send_email_bye
* search_restaurant{"location": "Delhi", "cuisine": "french"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
  - action_slot_reset
* search_restaurant{"location": "Delhi"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "french"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

<!-- invalid search -->

## interactive_story_83_greet_ask_location_valid_cuisine_valid_ask_budget_then_search_invalid
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_84_greet_location_valid_ask_cuisine_valid_ask_budget_then_search_invalid
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_85_greet_ask_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_then_search_invalid
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
  - action_slot_reset
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine  
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_86_greet_cuisine_valid_location_valid_ask_budget_then_search_invalid
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_87_greet_cuisine_invalid_retry_with_affirm_valid_ask_location_valid_ask_budget_then_search_invalid
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_88_greet_cuisine_valid_ask_location_invalid_retry_with_affirm_valid_ask_budget_then_search_invalid
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_89_greet_location_and_cuisine_together_valid_ask_budget_then_search_invalid
* greet
  - utter_greet
* search_restaurant{"location": "Mumbai", "cuisine": "chinese"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart
  
## interactive_story_90_greet_location_and_cuisine_together_cuisine_invalid_retry_with_affirm_valid_ask_budget_then_search_invalid
* greet
  - utter_greet
* search_restaurant{"location": "Mumbai", "cuisine": "chinese"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_91_greet_location_and_cuisine_together_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_then_search_invalid
* greet
  - utter_greet
* search_restaurant{"location": "Delhi", "cuisine": "french"}
  - action_location_valid
  - slot{"location_validity": "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location
* search_restaurant{"location": "Delhi"}
  - action_location_valid
  - slot{"location_validity": "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "french"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_92_greet_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_then_search_invalid
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_93_no_greet_location_valid_ask_cuisine_valid_ask_budget_then_search_invalid
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_94_no_greet_location_and_cuisine_together_valid_ask_budget_then_search_invalid
* search_restaurant{"cuisine":"indian","location":"Mysore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget":"high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_95_no_greet_location_and_cuisine_together_cuisine_invalid_retry_with_affirm_valid_ask_budget_then_search_invalid
* search_restaurant{"cuisine":"indian","location":"Mysore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget":"high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_96_no_greet_cuisine_valid_ask_location_valid_ask_budget_then_search_invalid
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_97_no_greet_cuisine_invalid_retry_with_affirm_valid_ask_location_valid_ask_budget_then_search_invalid
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_98_no_greet_cuisine_valid_ask_location_invalid_retry_with_affirm_valid_ask_budget_then_search_invalid
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_99_no_greet_location_and_cuisine_together_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_then_search_invalid
* search_restaurant{"location": "Delhi", "cuisine": "french"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location
* search_restaurant{"location": "Delhi"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "french"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_100_no_greet_location_invalid_retry_with_affirm_ask_cuisine_valid_ask_budget_then_search_invalid
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

## interactive_story_101_no_greet_location_invalid_retry_without_affirm_ask_cuisine_valid_ask_budget_then_search_invalid
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "invalid", "email_message": ""}
  - utter_search_invalid
  - utter_bye
  - action_restart

<!-- not helpful remark for bot -->

## interactive_story_102_greet_ask_location_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_103_greet_location_and_cuisine_together_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* greet
  - utter_greet
* search_restaurant{"location": "agra", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart
  
## interactive_story_104_greet_location_and_cuisine_together_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* greet
  - utter_greet
* search_restaurant{"location": "agra", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_105_greet_location_and_cuisine_together_location_invalid_retry_without_affirm_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* greet
  - utter_greet
* search_restaurant{"location": "agra", "cuisine": "italian"} 
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "agra"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_106_no_greet_location_and_cuisine_together_cuisine_invalid_retry_with_affirm_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* search_restaurant{"location": "agra", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_107_no_greet_location_and_cuisine_together_location_invalid_retry_without_affirm_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* search_restaurant{"location": "agra", "cuisine": "italian"} 
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* search_restaurant{"location": "agra"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}  
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_108_greet_cuisine_valid_ask_location_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_109_greet_cuisine_invalid_retry_with_affirm_valid_ask_location_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_110_greet_cuisine_valid_ask_location_invalid_retry_with_affirm_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_111_no_greet_cuisine_valid_ask_location_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_112_no_greet_cuisine_invalid_retry_with_affirm_valid_ask_location_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* affirm
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_113_no_greet_cuisine_valid_ask_location_invalid_retry_with_affirm_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_114_greet_location_and_cuisine_together_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* greet
  - utter_greet
* search_restaurant{"location": "Vizag", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location
* search_restaurant{"location": "Vizag"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "italian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_115_greet_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_116_greet_location_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_117_no_greet_location_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_118_no_greet_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_deny_email_then_bot_not_helpful
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* deny
  - utter_did_that_help
* deny
  - utter_sorry
  - utter_bye
  - action_restart

<!-- deny conversation -->

## interactive_story_119_greet_ask_location_invalid_ask_location_retry_then_deny
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* deny
  - utter_sorry
  - utter_bye
  - action_slot_reset
  - action_restart

## interactive_story_120_greet_ask_location_out_of_scope_ask_location_retry_then_deny
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* out_of_scope
  - action_slot_reset
  - utter_location_invalid
  - utter_ask_location_retry
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_121_greet_location_and_cuisine_together_cuisine_invalid_ask_cuisine_retry_then_deny
* greet
  - utter_greet
* search_restaurant{"location": "agra", "cuisine": "italian"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* deny
  - utter_sorry
  - utter_bye
  - action_slot_reset

## interactive_story_122_no_greet_location_and_cuisine_together_cuisine_invalid_ask_cuisine_retry_then_deny
* search_restaurant{"cuisine":"indian","location":"Mysore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_123_no_greet_location_invalid_ask_location_retry_then_deny
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_124_greet_location_invalid_ask_location_retry_then_deny
* greet
  - utter_greet
* search_restaurant{"location": "Patna"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_125_no_greet_cuisine_invalid_ask_cuisine_retry_then_deny
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_126_greet_cuisine_invalid_ask_cuisine_retry_then_deny
* greet
  - utter_greet
* search_restaurant{"cuisine": "indian"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_127_location_and_cuisine_together_location_invalid_ask_location_retry_then_deny
* search_restaurant{"location":"Kolkata", "cuisine":"mexican"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* deny
  - utter_sorry
  - utter_bye
  - action_restart

## interactive_story_128_location_and_cuisine_together_cuisine_invalid_ask_cuisine_retry_then_deny
* search_restaurant{"location":"Kolkata", "cuisine":"mexican"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "invalid"}
  - utter_cuisine_invalid
  - utter_ask_cuisine_retry
* deny
  - utter_sorry
  - utter_bye
  - action_restart

<!-- stop conversation -->

## interactive_story_129_greet_then_bye
* greet
  - utter_greet
* bye
  - utter_bye
  - action_restart

## interactive_story_130_greet_ask_location_then_bye
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* bye
  - utter_bye
  - action_restart

## interactive_story_131_no_greet_ask_location_then_bye
* search_restaurant
  - utter_ask_location
* bye
  - utter_bye
  - action_restart

## interactive_story_132_no_greet_location_invalid_ask_location_retry_then_bye
* search_restaurant{"location": "delhi"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* bye
  - utter_bye
  - action_restart

## interactive_story_133_no_greet_ask_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_then_bye
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "delhi"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* bye
  - utter_bye
  - action_restart

## interactive_story_134_no_greet_location_invalid_retry_with_affirm_valid_ask_cuisine_then_bye
* search_restaurant{"location": "delhi"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* bye
  - utter_bye
  - action_restart

## interactive_story_135_no_greet_ask_location_invalid_retry_with_affirm_then_bye
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "delhi"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location
* bye
  - utter_bye
  - action_restart

## interactive_story_136_no_greet_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_then_bye
* search_restaurant{"location": "delhi"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* bye
  - utter_bye
  - action_restart

<!-- handle out of scope responses -->

## interactive_story_137_greet_then_out_of_scope
* greet
  - utter_greet
* out_of_scope
  - utter_out_of_scope
  - utter_bye
  - action_restart

## interactive_story_138_no_greet_ask_location_out_of_scope_ask_location_retry_then_again_out_of_scope
* search_restaurant
  - utter_ask_location
* out_of_scope
  - utter_location_invalid
  - utter_ask_location_retry
* out_of_scope
  - utter_bye
  - action_restart

## interactive_story_139_no_greet_location_invalid_ask_location_retry_then_out_of_scope
* search_restaurant{"location": "delhi"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* out_of_scope
  - utter_bye
  - action_restart

## interactive_story_140_no_greet_location_and_cuisine_together_location_invalid_ask_location_retry_then_out_of_scope
* search_restaurant{"location":"Kolkata", "cuisine":"mexican"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* out_of_scope
  - utter_bye
  - action_restart

## interactive_story_141_no_greet_ask_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_out_of_scope_again_ask_email_deny_email_bye
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "delhi"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* out_of_scope
  - utter_ask_details
* deny
  - utter_bye
  - action_restart

## interactive_story_142_no_greet_ask_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_out_of_scope_again_ask_email_with_affirm_send_email_bye
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "delhi"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* out_of_scope
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_143_no_greet_location_and_cuisine_together_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_out_of_scope_again_ask_email_with_affirm_send_email_bye
* search_restaurant{"location":"Kolkata", "cuisine":"mexican"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine":"mexican"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* out_of_scope
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_144_no_greet_location_and_cuisine_together_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_out_of_scope_again_ask_email_deny_email_bye
* search_restaurant{"location":"Kolkata", "cuisine":"mexican"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine":"mexican"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* out_of_scope
  - utter_ask_details
* deny
  - utter_bye
  - action_restart

## interactive_story_145_no_greet_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_out_of_scope_again_ask_email_without_affirm_send_email_bye
* search_restaurant{"location": "delhi"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "mid_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* out_of_scope
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_146_no_greet_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_out_of_scope_again_ask_email_deny_email_bye
* search_restaurant{"location": "delhi"}
  - action_location_valid
  - slot{"location_validity" : "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "mid_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* out_of_scope
  - utter_ask_details
* deny
  - utter_bye
  - action_restart

## interactive_story_147_no_greet_location_and_cuisine_together_valid_ask_budget_ask_email_out_of_scope_again_ask_email_with_affirm_send_email_bye
* search_restaurant{"location":"Kolkata", "cuisine":"mexican"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* out_of_scope
  - utter_ask_details
* affirm
  - utter_ask_email
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
  - utter_bye
  - action_restart

## interactive_story_148_no_greet_location_and_cuisine_together_valid_ask_budget_ask_email_out_of_scope_again_ask_email_deny_email_bye
* search_restaurant{"location":"Kolkata", "cuisine":"mexican"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* out_of_scope
  - utter_ask_details
* deny
  - utter_bye
  - action_restart

<!-- direct email address without affirm -->

## interactive_story_149_greet_location_and_cuisine_together_valid_ask_budget_ask_email_without_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant{"location": "Mumbai", "cuisine": "chinese"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_150_no_greet_location_and_cuisine_together_valid_ask_budget_ask_email_without_affirm_send_email_thank
* search_restaurant{"cuisine":"indian","location":"Mysore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}  
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget":"high_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_151_greet_ask_location_valid_ask_cuisine_valid_ask_budget_ask_email_without_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_152_greet_ask_location_out_of_scope_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_without_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant
  - utter_ask_location
* out_of_scope
  - action_slot_reset
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location  
* search_restaurant{"location": "Bangalore"}
  - action_location_valid
  - slot{"location_validity" : "valid"}
  - utter_ask_cuisine  
* search_restaurant{"cuisine": "Chinese"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity" : "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

## interactive_story_153_greet_location_and_cuisine_together_location_invalid_retry_with_affirm_valid_ask_cuisine_valid_ask_budget_ask_email_without_affirm_send_email_thank
* greet
  - utter_greet
* search_restaurant{"location": "Delhi", "cuisine": "french"}
  - action_location_valid
  - slot{"location_validity": "invalid"}
  - utter_location_invalid
  - utter_ask_location_retry
* affirm
  - action_slot_reset
  - utter_ask_location
* search_restaurant{"location": "Delhi"}
  - action_location_valid
  - slot{"location_validity": "valid"}
  - utter_ask_cuisine
* search_restaurant{"cuisine": "french"}
  - action_cuisine_valid
  - slot{"cuisine_validity" : "valid"}
  - utter_ask_budget
* ask_budget{"budget": "low_budget"}
  - action_search_restaurant
  - slot{"search_validity": "valid", "email_message": ""}
  - utter_ask_details
* ask_email{"email": "abc@abc.com"}
  - action_send_email
  - utter_confirm_email
* thank
  - utter_bye
  - action_restart

<!-- markdownlint-restore -->
