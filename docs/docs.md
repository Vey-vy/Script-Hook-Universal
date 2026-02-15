# ScriptHook API Documentation

## GTA V
```cpp
script_register                    // Register main script thread
script_register_another_thread     // Register additional thread
script_unregister                  // Unregister script
native_call_begin                  // Initialize native call
native_push                        // Push parameter to native
native_call                        // Execute native and get result
get_global_ptr                     // Get pointer to global variable
create_texture                     // Load texture from file
draw_texture                       // Draw texture on screen
script_wait                        // Pause script execution
keyboard_handler_register          // Register keyboard callback
keyboard_handler_unregister        // Unregister keyboard callback
get_game_verison                   // Get current game version
get_script_handle_base_adress      // Get entity base address
present_call_back_register         // Register present callback
present_call_back_unregister       // Unregister present callback
world_get_all_vehicles             // Get all vehicle handles
world_get_all_peds                 // Get all ped handles
world_get_all_objects              // Get all object handles
world_get_all_pickups              // Get all pickup handles
register_raw_streaming_file        // Register custom streaming file
```

---

## Red Dead Redemption 2
```cpp
script_register                    // Register main script thread
script_register_another_thread     // Register additional thread
script_unregister                  // Unregister script
native_call_begin                  // Initialize native call
native_push                        // Push parameter to native
native_call                        // Execute native and get result
get_global_ptr                     // Get pointer to global variable
create_texture                     // Load texture from file
draw_texture                       // Draw texture on screen
script_wait                        // Pause script execution
keyboard_handler_register          // Register keyboard callback
keyboard_handler_unregister        // Unregister keyboard callback
get_game_verison                   // Get current game version
get_script_handle_base_adress      // Get entity base address
present_call_back_register         // Register present callback
present_call_back_unregister       // Unregister present callback
world_get_all_vehicles             // Get all vehicle handles
world_get_all_peds                 // Get all ped handles
world_get_all_objects              // Get all object handles
world_get_all_pickups              // Get all pickup handles
```

## Red Dead Redemption
```cpp
script_register                    // Register main script thread
script_register_another_thread     // Register additional thread
script_unregister                  // Unregister script
native_call_begin                  // Initialize native call
native_push                        // Push parameter to native
native_call                        // Execute native and get result
print                              // Log message to console
rh_load_image                      // Load image from file path
rh_draw_image                      // Draw image on screen
rh_draw_rect                       // Draw rectangle on screen
rh_draw_text                       // Draw text on screen
rh_get_text_width                  // Calculate text width
rh_get_text_height                 // Calculate text height
rh_set_text_wrap_width             // Set text wrapping width
rh_action_disable                  // Disable game action
rh_get_minor_version               // Get RedHook minor version
rh_get_major_version               // Get RedHook major version
```

---

## Max Payne 3 (32-bit)
```cpp
script_register                    // Register main script thread
script_register_another_thread     // Register additional thread
script_unregister                  // Unregister script
native_call_begin                  // Initialize native call
native_push                        // Push parameter to native
native_call                        // Execute native and get result
get_global_ptr                     // Get pointer to global variable
script_wait                        // Pause script execution
keyboard_handler_register          // Register keyboard callback
keyboard_handler_unregister        // Unregister keyboard callback
world_get_all_vehicles             // Get all vehicle handles
world_get_all_peds                 // Get all ped handles
world_get_all_objects              // Get all object handles
world_get_all_interiors            // Get all interior handles
world_get_all_blips                // Get all blip handles
get_blip_address                   // Get blip memory address
get_interior_address               // Get interior memory address
get_object_address                 // Get object memory address
get_ped_address                    // Get ped memory address
get_vehicle_address                // Get vehicle memory address
```