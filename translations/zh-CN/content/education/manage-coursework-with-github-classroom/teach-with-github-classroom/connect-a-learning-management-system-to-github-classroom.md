---
title: 将学习管理系统连接到 GitHub Classroom
intro: 您可以配置 LTI 兼容的学习管理系统 (LMS) 连接到 {% data variables.product.prodname_classroom %}，以便导入用于课堂的名册。
versions:
  fpt: '*'
permissions: Organization owners who are admins for a classroom can connect learning management systems to {% data variables.product.prodname_classroom %}. {% data reusables.classroom.classroom-admins-link %}
redirect_from:
- /education/manage-coursework-with-github-classroom/configuring-a-learning-management-system-for-github-classroom
- /education/manage-coursework-with-github-classroom/connect-to-lms
- /education/manage-coursework-with-github-classroom/generate-lms-credentials
- /education/manage-coursework-with-github-classroom/setup-canvas
- /education/manage-coursework-with-github-classroom/setup-generic-lms
- /education/manage-coursework-with-github-classroom/setup-moodle
- /education/manage-coursework-with-github-classroom/connect-a-learning-management-system-to-github-classroom
shortTitle: Connect an LMS
ms.openlocfilehash: 4138d2e63860815cdba41e6f30209f0bf637104d
ms.sourcegitcommit: 22d665055b1bee7a5df630385e734e3a149fc720
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/13/2022
ms.locfileid: "145097937"
---
## <a name="about-configuration-of-your-lms"></a>关于 LMS 的配置

您可以将学习管理系统 (LMS) 连接到 {% data variables.product.prodname_classroom %}，然后 {% data variables.product.prodname_classroom %} 可以从 LMS 导入学生标识符名册。 若要将 LMS 连接到 {% data variables.product.prodname_classroom %}，必须在 LMS 中输入 {% data variables.product.prodname_classroom %} 的配置凭据。

## <a name="prerequisites"></a>先决条件

要配置 LMS 连接到 {% data variables.product.prodname_classroom %}，您必须先创建一个教室。 有关详细信息，请参阅“[管理教室](/education/manage-coursework-with-github-classroom/manage-classrooms#creating-a-classroom)”。

## <a name="supported-lmses"></a>支持的 LMSes

{% data variables.product.prodname_classroom %} 支持从实施学习工具互操作性 (LTI) 标准的 LMS 导入名册数据。

- LTI 版本 1.0 和/或 1.1
- 配置 1.X 的 LTI 名称和角色

使用 LTI 有助于确保您的信息安全。 LTI 是一个行业标准协议，GitHub Classroom 对 LTI 的使用得到了教学管理系统 (IMS) 全球学习联盟的认证。 有关详细信息，请参阅 IMS 全球学习联盟网站上的[学习工具互操作性](https://www.imsglobal.org/activity/learning-tools-interoperability)和[关于 IMS 全球学习联盟](http://www.imsglobal.org/aboutims.html)。

{% data variables.product.company_short %} 测试了名册数据从以下 LMS 到 {% data variables.product.prodname_classroom %} 的导入。

- 画布
- Google Classroom
- Moodle
- Sakai

目前，{% data variables.product.prodname_classroom %} 不支持从 Blackboard 或 Brightspace 导入名册数据。

## <a name="generating-configuration-credentials-for-your-classroom"></a>为教室生成配置凭据

{% data reusables.classroom.sign-into-github-classroom %} {% data reusables.classroom.click-classroom-in-list %} {% data reusables.classroom.click-students %}
1. 如果您的教室已有名册，您可以更新名册或删除名册并创建新的名册。
    - 有关删除和创建名册的详细信息，请参阅“[删除教室名册](/education/manage-coursework-with-github-classroom/manage-classrooms#deleting-a-roster-for-a-classroom)”和“[为教室创建名册](/education/manage-coursework-with-github-classroom/manage-classrooms#creating-a-roster-for-your-classroom)”。
    - 有关更新名册的详细信息，请参阅“[将学生添加到教室名册](/education/manage-coursework-with-github-classroom/manage-classrooms#adding-students-to-the-roster-for-your-classroom)”。
1. 在 LMS 列表中，单击您的 LMS。 如果你的 LMS 不受支持，请单击“其他 LMS”。
  ![LMS 列表](/assets/images/help/classroom/classroom-settings-click-lms.png)
1. 阅读有关连接 LMS 的信息，然后单击“连接到 LMS”。
1. 复制用于连接到教室的“消费者密钥”、“共享密钥”和“启动 URL”。
  ![复制凭据](/assets/images/help/classroom/classroom-copy-credentials.png)

## <a name="configuring-a-generic-lms"></a>配置通用 LMS

您必须为 LMS 配置隐私设置，以允许外部工具接收名册信息。

1. 导航到 LMS。
1. 配置外部工具。
1. 提供您在 {% data variables.product.prodname_classroom %} 中生成的配置凭据。
    - 使用者密钥
    - 共享密钥
    - 启动 URL（有时称为“工具 URL”或类似名称）

## <a name="configuring-canvas"></a>配置 Canvas

您可以将 {% data variables.product.prodname_classroom %} 配置为 Canvas 的外部应用以将名册数据导入到您的教室。 有关 Canvas 的详细信息，请参阅 [Canvas 网站](https://www.instructure.com/canvas/)。

1. 登录到 [Canvas](https://www.instructure.com/canvas/#login)。
1. 选择要与 {% data variables.product.prodname_classroom %} 集成的 Canvas 课程。
1. 在左侧边栏中，单击“设置”。
1. 单击“应用”选项卡。
1. 单击“查看应用配置”。
1. 单击“+ 应用”。
1. 选择“配置类型”下拉菜单，然后单击“按 URL” 。
1. 从 {% data variables.product.prodname_classroom %} 粘贴配置凭据。 有关详细信息，请参阅“[为教室生成配置凭据](#generating-configuration-credentials-for-your-classroom)”。

    | Canvas 应用程序配置中的字段 | 值或设置 |
    | :- | :- |
    | **使用者密钥** | {% data variables.product.prodname_classroom %} 中的消费者密钥 |
    | **共享密钥** | {% data variables.product.prodname_classroom %} 中的共享密钥 |
    | **允许此工具访问 IMS 名称和角色预配服务** | 已启用 |
    | 配置 URL | {% data variables.product.prodname_classroom %} 中的启动 URL |

    {% note %}

    注意：如果在 Canvas 中看不到标有“允许此工具访问 IMS 名称和角色配置服务”的复选框，则你的 Canvas 管理员必须联系 Canvas 支持人员，以便为你的 Canvas 帐户启用成员身份服务配置。 如果不启用此功能，您将无法从 Canvas 同步名册。 有关详细信息，请参阅 Canvas 网站上的[如何联系 Canvas 支持人员？](https://community.canvaslms.com/t5/Canvas-Basics-Guide/How-do-I-contact-Canvas-Support/ta-p/389767)。

    {% endnote %}

1. 单击“提交”  。
1. 在左边栏中，单击“主页”。
1. 要提示 Canvas 发送确认电子邮件，请在左边栏中单击“GitHub Classroom”。 按照电子邮件中的说明完成链接 {% data variables.product.prodname_classroom %}。

## <a name="configuring-moodle"></a>配置 Moodle

您可以将 {% data variables.product.prodname_classroom %} 配置为 Moodle 的活动以将名册数据导入到您的教室。 有关 Moodle 的详细信息，请参阅 [Moodle 网站](https://moodle.org)。

您必须使用 Moodle 版本 3.0 或更高版本。

1. 登录到 [Moodle](https://moodle.org/login/)。
1. 选择要与 {% data variables.product.prodname_classroom %} 集成的 Moodle 课程。
1. 单击“启用编辑”。
1. 如果希望 {% data variables.product.prodname_classroom %} 在 Moodle 中可用，请单击“添加活动或资源”。
1. 选择“外部工具”，然后单击“添加” 。
1. 在“Activity name（活动名称）”字段中，键入 "GitHub Classroom"。
1. 在“预配置的工具”字段中，单击下拉菜单右侧的“+” 。
1. 在“External tool configuration（外部工具配置）”下，从 {% data variables.product.prodname_classroom %} 粘贴配置凭据。 有关详细信息，请参阅“[为教室生成配置凭据](#generating-configuration-credentials-for-your-classroom)”。

    | Moodle 应用程序配置中的字段 | 值或设置 |
    | :- | :- |
    | **工具名称** | {% data variables.product.prodname_classroom %} - 你的教室名称<br/><br/>注意：可以使用任何名称，但为了清楚起见，我们建议使用此值。 |
    | 工具 URL | {% data variables.product.prodname_classroom %} 中的启动 URL |
    | LTI 版本 | LTI 1.0/1.1 |
    | 默认启动容器 | 新建窗口 |
    | 使用者密钥 | {% data variables.product.prodname_classroom %} 中的消费者密钥 |
    | 共享机密 | {% data variables.product.prodname_classroom %} 中的共享密钥 |

1. 滚动到“服务”并单击它。
1. 在“IMS LTI 名称和角色预配”右侧，选择下拉菜单并单击“根据隐私设置使用此服务检索成员信息”。
1. 滚动到“隐私”并单击它。
1. 在“与工具共享启动者的名称”和“与工具共享启动者的电子邮件”右侧，选择下拉菜单并单击“始终”  。
1. 在页面的底部，单击“保存更改”。
1. 在“预配置工具”菜单中，单击“GitHub Classroom - 你的教室名称” 。
1. 在“通用模块设置”下“可用性”的右侧，选择下拉菜单并单击“对学生隐藏”。
1. 在页面底部，单击“保存并返回到课程”。
1. 导航到您选择显示 {% data variables.product.prodname_classroom %} 的任何位置，然后单击 {% data variables.product.prodname_classroom %} 活动。

## <a name="importing-a-roster-from-your-lms"></a>从 LMS 导入名册

有关将名册从 LMS 导入 {% data variables.product.prodname_classroom %} 的详细信息，请参阅“[管理教室](/education/manage-coursework-with-github-classroom/manage-classrooms#creating-a-roster-for-your-classroom)”。

## <a name="disconnecting-your-lms"></a>断开 LMS 连接

{% data reusables.classroom.sign-into-github-classroom %} {% data reusables.classroom.click-classroom-in-list %} {% data reusables.classroom.click-settings %}
1. 在“连接到学习管理系统(LMS)”下，单击“连接设置”。
  ![教室设置中的“连接设置”链接](/assets/images/help/classroom/classroom-settings-click-connection-settings.png)
1. 在“删除与学习管理系统的连接”下，单击“断开与学习管理系统的连接”。
  ![教室连接设置中的“与学习管理系统断开连接”按钮](/assets/images/help/classroom/classroom-settings-click-disconnect-from-your-lms-button.png)
