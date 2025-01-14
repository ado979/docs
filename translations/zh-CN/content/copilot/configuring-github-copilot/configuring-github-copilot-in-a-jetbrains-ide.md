---
title: 在 JetBrains IDE 中配置 GitHub Copilot
intro: '可以在 JetBrains IDE 中启用、配置和禁用 {% data variables.product.prodname_copilot %}。'
product: '{% data reusables.gated-features.copilot %}'
topics:
  - Copilot
versions:
  feature: copilot
shortTitle: JetBrains
ms.openlocfilehash: 9f0f35bf5aebbf1899bd3991b0bca9e62f1da6ed
ms.sourcegitcommit: 6185352bc563024d22dee0b257e2775cadd5b797
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2022
ms.locfileid: '148193252'
---
## 关于 JetBrains IDE 中的 {% data variables.product.prodname_copilot %}

如果使用 Jetbrains IDE，{% data variables.product.prodname_copilot %} 可在你键入内容时自动完成代码。 安装后，可以启用或禁用 {% data variables.product.prodname_copilot %}，并且可以在 IDE 或 {% data variables.product.prodname_dotcom_the_website %} 上配置高级设置。 本文介绍如何在 IntelliJ IDE 中配置 {% data variables.product.prodname_copilot %}，但其他 Jetbrains IDE 的用户界面可能有所不同。

{% data reusables.copilot.dotcom-settings %}

## 先决条件

要在 JetBrains IDE 中配置 {% data variables.product.prodname_copilot %}，必须先安装 {% data variables.product.prodname_copilot %} 插件。 有关详细信息，请参阅“[JetBrains IDE 中的 {% data variables.product.prodname_copilot %} 入门指南](/copilot/getting-started-with-github-copilot/getting-started-with-github-copilot-in-a-jetbrains-ide)”。

## {% data variables.product.prodname_copilot %} 的键盘快捷方式

使用 {% data variables.product.prodname_copilot %} 时，可以在 JetBrains IDE 中使用默认键盘快捷方式获取内联建议。 或者，可以将快捷方式重新绑定到每个特定命令的首选键盘快捷方式。 有关在 JetBrains IDE 中重新绑定键盘快捷方式的详细信息，请参阅 JetBrains 文档。 例如，可以查看 [IntelliJ IDEA](https://www.jetbrains.com/help/idea/mastering-keyboard-shortcuts.html#choose-keymap) 文档。

{% mac %}

| 操作 | 快捷键 |
|:---|:---|
|接受内联建议|<kbd>选项卡</kbd>|
|忽略内联建议|<kbd>Esc</kbd>|
|显示下一个内联建议|<kbd>Option (⌥) 或 Alt</kbd>+<kbd>]</kbd>|
|显示上一个内联建议|<kbd>Option (⌥) 或 Alt</kbd>+<kbd>[</kbd>|
|触发内联建议|<kbd>Option (⌥)</kbd>+<kbd>\</kbd>|
|打开 {% data variables.product.prodname_copilot %}（单独窗格中的其他建议）|<kbd>Option (⌥) 或 Alt</kbd>+<kbd>Return</kbd> |

{% endmac %}

{% windows %}

| 操作 | 快捷键 |
|:---|:---|
|接受内联建议|<kbd>选项卡</kbd>|
|忽略内联建议|<kbd>Esc</kbd>|
|显示下一个内联建议|<kbd>Alt</kbd>+<kbd>]</kbd>|
|显示上一个内联建议|<kbd>Alt</kbd>+<kbd>[</kbd>|
|触发内联建议|<kbd>Alt</kbd>+<kbd>\</kbd>|
|打开 {% data variables.product.prodname_copilot %}（单独窗格中的其他建议）|<kbd>Alt</kbd>+<kbd>Enter</kbd> |

{% endwindows %}

{% linux %}

| 操作 | 快捷键 |
|:---|:---|
|接受内联建议|<kbd>选项卡</kbd>|
|忽略内联建议|<kbd>Esc</kbd>|
|显示下一个内联建议|<kbd>Alt</kbd>+<kbd>]</kbd>|
|显示上一个内联建议|<kbd>Alt</kbd>+<kbd>[</kbd>|
|触发内联建议|<kbd>Alt</kbd>+<kbd>\</kbd>|
|打开 {% data variables.product.prodname_copilot %}（单独窗格中的其他建议）|<kbd>Alt</kbd>+<kbd>Enter</kbd> |

{% endlinux %}

## 启用或禁用 {% data variables.product.prodname_copilot %}

可从 JetBrains IDE 启用或禁用 {% data variables.product.prodname_copilot %}。 JetBrains 窗口底部面板中的 {% data variables.product.prodname_copilot %} 状态图标指示 {% data variables.product.prodname_copilot %} 是启用还是禁用。 启用后，将突出显示图标。 禁用后，图标灰显。

1. 若要启用或禁用 {% data variables.product.prodname_copilot %}，请单击 JetBrains 窗口底部面板中的状态图标。
   ![JetBrains 中的状态图标](/assets/images/help/copilot/status-icon-jetbrains.png)
2. 如果要禁用 {% data variables.product.prodname_copilot %}，系统会询问是全局禁用它，还是要禁用当前正在编辑的文件的语言。 若要全局禁用，请单击“禁用完成”。 或者，单击特定于语言的按钮，为指定语言禁用 {% data variables.product.prodname_copilot %}。
   ![全局或为当前语言禁用 {% data variables.product.prodname_copilot %}](/assets/images/help/copilot/disable-copilot-global-or-langugage-jetbrains.png)

## 配置 {% data variables.product.prodname_copilot %} 的高级设置

可在 JetBrains IDE 中管理 {% data variables.product.prodname_copilot %} 的高级设置，例如 IDE 显示代码完成的方式，以及针对 {% data variables.product.prodname_copilot %} 要启用或禁用的语言。

1. 在 JetBrains IDE 中，单击“文件”菜单，然后单击“设置” 。
1. 在“语言和框架”下，单击 {% data variables.product.prodname_copilot %} 。
1. 根据个人首选项编辑设置。
   - 要调整代码建议的行为和外观，以及是否自动检查更新，请选中或取消选中相应的复选框。
   - 如果已选择接收自动更新，可以选择是接收稳定但频率较低的更新，还是接收可能不太稳定的夜间更新。 单击“更新通道”下拉列表，选择“稳定”（适用于稳定更新）或“夜间”（适用于夜间更新）  。
   - 在“已禁用的语言”下，使用复选框选择或取消选择要为其禁用 {% data variables.product.prodname_copilot %} 的语言。

## 配置 {% data variables.product.prodname_copilot %} 的代理设置

可以将 {% data variables.product.prodname_copilot %} 配置为通过 Jetbrains IDE 中的 HTTP 代理服务器进行连接。 {% data variables.product.prodname_copilot %} 支持基本 HTTP 代理设置，无论是否使用基本身份验证。 

1. 在 JetBrains IDE 中，单击“文件”菜单，然后单击“设置” 。
1. 在“外观与行为”下，单击“系统设置”，然后单击“HTTP 代理”  。
1. 选中“手动代理配置”复选框，然后选中“HTTP”复选框 。
1. 在“主机名”字段中，输入代理服务器的主机名，并在“端口号”字段中输入代理服务器的端口号。

    ![JetBrains 中 HTTP 代理设置的屏幕截图](/assets/images/help/copilot/proxy-configuration-jetbrains.png)

1. （可选）在左侧边栏中，单击“工具”，然后单击“服务器证书” 。 然后，根据是否要自动接受不受信任的证书，选中或取消选中“自动接受不受信任的证书”复选框。

    ![JetBrains 中服务器证书设置的屏幕截图](/assets/images/help/copilot/server-certificates-jetbrains.png)

{% data reusables.copilot.dotcom-settings %}
