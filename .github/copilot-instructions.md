# GitHub Copilot Instructions for EDS Development

## Context
This is an Adobe Experience Manager Edge Delivery Services (EDS) project for Owens Corning.
Full documentation: https://www.aem.live/llms.txt

## Code Patterns
- Blocks use vanilla JS with `export default function decorate(block) {}`
- No frameworks, no build tools, no npm
- CSS uses custom properties defined in /styles/styles.css and /styles/brand.css
- Content is authored in Word/Google Docs, not in code

## File Naming
- Block folder: /blocks/{block-name}/
- Block JS: /blocks/{block-name}/{block-name}.js
- Block CSS: /blocks/{block-name}/{block-name}.css
- Block models (UE): /blocks/{block-name}/component-definition.json

## Testing
- Preview: https://main--poc-cr-owens-corning--aemxsc.aem.live
- Admin: https://admin.da.live/#/aemxsc/poc-cr-owens-corning
