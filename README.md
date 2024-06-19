# Magento 2 Module to Disable CSP

This Magento 2 module provides a simple solution to disable the Content Security Policy (CSP) enforcement in the 
checkout process, which was introduced in the security update on 2024-06-11 and caused issues for many merchants.

## Installation

Install the module via Composer:

`composer require wouyang/module-disable-csp`


## How it Works

After installation, this module disables the following two events responsible for enforcing CSP in the checkout process:

- `layout_render_before_csp_can_render_instructions`
- `layout_render_before_csp_can_render_instructions_checkout`

By disabling these events, you can effectively bypass the CSP enforcement without completely disabling the `Module_Csp`, which may still be required for other functionalities or security measures in your Magento store.

## Usage

No further configuration is required. The module will automatically disable the specified events upon installation.

## Compatibility

This module is compatible with Magento 2.4.7-p1, 2.4.6-p6, 2.4.5-p8, 2.4.4-p9 and later versions.

## Support

If you encounter any issues or have questions, please open an issue on the [GitHub repository](https://github.com/weiweiouyang/magento2-module-disable-csp).

## License

This module is licensed under the [MIT License](LICENSE).
