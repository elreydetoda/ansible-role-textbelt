[![Build Status](https://travis-ci.com/elreydetoda/ansible-role-textbelt.svg?branch=master)](https://travis-ci.com/elreydetoda/ansible-role-textbelt)

# ansible-role-textbelt

> Textbelt is a no-nonsense SMS API built for developers who just want to send SMS. Thousands of clients prefer Textbelt over other SMS providers for our ease of setup, simple, predictable pricing packages, and personal support.

## Requirements

You will need an API key from textbelt.com or if you are [self hosting](https://github.com/typpo/textbelt). You will also need a phone number for where you are sending the message to. You will probably want to customize teh message as well.

For more about textbelt api calls, visit [here](https://docs.textbelt.com/)

## Role Variables

### Required

- `api_key` - the textbelt api key (vars/main.yml)
- `phone_number` - phone number to send message to  (vars/main.yml)

### Optional

- `textbelt_url` - api endpoint which to send the request to: `https://textbelt.com/text` (defaults/main.yml)
- `message_contents` - the message you want to send: `this is a test. nicely done :D` (defaults/main.yml)
- `quota_warning_number` - the number you want to be notified for when your textbelt quota left is less than: `100` (defaults/main.yml)

## Dependencies

This role only uses the [uri module](https://docs.ansible.com/ansible/latest/modules/uri_module.html). So, whatever dependencies are necessary for that.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yaml
    - hosts: servers
      roles:
         - { role: elreydetoda.ansible_role_textbelt, api_key: xyz, phone_number: +xxxxxxxxxxx }
```

## License

MIT

## Author Information

[https://elrey.casa/blog](https://elrey.casa/blog)
