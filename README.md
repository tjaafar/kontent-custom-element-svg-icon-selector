# SVG Icon Selector Custom Element for Kentico Kontent

This is a [custom element](https://docs.kontent.ai/tutorials/develop-apps/integrate/integrating-your-own-content-editing-features) for [Kentico Kontent](https://kontent.ai) that allows users to select an SVG icon from a list of provided icons.

![Screenshot of custom element](SvgIconSelector.png)

## Setup

1. Deploy the code to a secure public host
    * See [deploying section](#Deploying) for a really quick option
1. Follow the instructions in the [Kentico Kontent documentation](https://docs.kontent.ai/tutorials/develop-apps/integrate/integrating-your-own-content-editing-features#a-3--displaying-a-custom-element-in-kentico-kontent) to add the element to a content model.
    * The `Hosted code URL` is where you deployed to in step 1
    * Pass the necessary parameters as directed in the [JSON Parameters configuration](#json-parameters) section of this readme.

## Deploying

Netlify has made this easy. If you click the deploy button below, it will guide you through the process of deploying it to Netlify and leave you with a copy of the repository in your GitHub account as well.

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/Kentico/kontent-custom-element-svg-icon-selector)

## JSON Parameters

The main `controlLabel` parameter is used to show the text on the dropdown.

You have to configure `controlLabel` and `options` parameters. There should be at least two options for this to work.

Here's an example with five options provided:

```Json
{
  "controlLabel": "Please select an OSA icon",
  "options": [
    {
      "label": "Firewall",
      "value": "firewall",
      "icon": "/icons/osa_firewall.svg"
    },
    {
      "label": "Home",
      "value": "home",
      "icon": "/icons/osa_home.svg"
    },
    {
      "label": "Architect",
      "value": "architect",
      "icon": "/icons/osa_user_green_architect.svg"
    },
    {
      "label": "Project Manager",
      "value": "projectManager",
      "icon": "/icons/osa_user_green_project_manager.svg"
    },
    {
      "label": "Security Specialist",
      "value": "security-specialist",
      "icon": "/icons/osa_user_blue_security_specialist.svg"
    }
  ]
}
```

## Saved Value

The value is saved as a string representing the specified value of the selected option.

## Contributors

Originally contributed by [@emmanueltissera](https://github.com/emmanueltissera/)
