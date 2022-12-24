Not ready for prime time!  (Incomplete and undocumented, and most of things dont works, prbably because they changed the API)

This code is utterly untested, but will get you pointed in the right direction.

    mothership_url = "http://www.wherever.org:8080"
    thingsboard_username = "who_are_you"
    thingsboard_password = "xyzzy"

    tbapi = TbApi(mothership_url, thingsboard_username, thingsboard_password)

    device = tbapi.get_device_by_name("device_name")
    
    latest_temp = tbapi.get_latest_telemetry(device, "temperature")
    all_humidity = tbapi.get_telemetry(device, "humidity")     # Lots more options on this method



