+++
title = 'Aside'
weight = 40
layout = 'aside'

[cascade]
layout = 'aside'

[[sidebar]]
title = 'Getting started'
[[sidebar.links]]
page = '/docs/aside'
title = 'Overview'
[[sidebar.links]]
page = '/docs/aside/layout'
[[sidebar.links]]
title = 'Example'
url = 'https://example.com'

[[sidebar]]
title = 'Elements'
[[sidebar.links]]
page = '/docs/aside/text'
[[sidebar.links]]
page = '/docs/aside/inputs'

[[sidebar]]
title = 'Components'
[[sidebar.links]]
page = '/docs/aside/table'
[[sidebar.links]]
page = '/docs/aside/accordion'
+++

Choose an item in the sidebar to visit its page. The current link uses `aria-current="page"`, styled by the stylesheet. Each page has its own URL, so you can bookmark it or use the browser's Back button.

{{< lorem >}}
