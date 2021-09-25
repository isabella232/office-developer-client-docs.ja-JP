---
title: Web サーバー コンピューターにゲスト特権を付与する。RDS ゲスト特権
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: df3b2043dbfc9fe09b842f999db3e40f5e5ec2b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577326"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Web サーバー コンピューターにゲスト特権を付与する。RDS ゲスト特権

**適用先:** Access 2013、Office 2013

RDS を使用するには、匿名 Web サーバー アカウント (IUSR ComputerName) を Web サーバー コンピューターのゲスト ローカル グループに \_ 追加する必要があります。

**Web サーバー コンピューターにゲスト特権を付与するには**

1.  Microsoft Windows 2000 Server コンピューターで、[スタート] をクリックし、[プログラム]をポイントし、[管理ツール] をポイントし、[コンピューターの管理]**をクリックします**。

2.  In the console tree, in **Local Users and Groups**, click **Groups**.

3.  Select the **Guests** local group. From the **Action** menu, choose **Properties**.

4.  In the **Guests Properties** dialog box, click **Add**.

5.  [ユーザーまたはグループの選択] ダイアログ ボックスの一覧に匿名 Web サーバー アカウントが表示されない場合は、その名前 (IUSR \_ *ComputerName)* を下部の空白ボックスに入力し、[追加] をクリック **します**。

6.  [**OK**] をクリックします。

