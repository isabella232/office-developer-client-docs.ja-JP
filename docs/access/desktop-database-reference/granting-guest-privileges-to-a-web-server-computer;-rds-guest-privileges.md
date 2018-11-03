---
title: Web サーバー コンピューターにゲストの特権を付与します。RDS ゲスト権限
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f1f127e4ea9393d3b461e9b7da2901df554ee36b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947211"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a>Web サーバー コンピューターにゲストの特権を付与します。RDS ゲスト権限

**適用されます**Access 2013、Office 2013。

匿名 web サーバー アカウント (IUSR\_*コンピューター名*) RDS を使用する web サーバー コンピューターの Guests ローカル グループに追加する必要があります

**Web サーバー コンピューターへのゲストの特権を付与するには**

1.  Microsoft Windows 2000 Server コンピューターに [**スタート**] ボタン、**プログラム**] をポイント **[管理ツール**] をポイントし、し、[**コンピューターの管理**] をクリックします。

2.  コンソール ツリーで、**ローカル ユーザーとグループ**は、[**グループ**] をクリックします。

3.  **Guests**ローカル グループを選択します。 **[操作**] メニューから**プロパティ**を選択します。

4.  **Guests のプロパティ**] ダイアログ ボックスで、[**追加**を] をクリックします。

5.  匿名 web サーバー アカウントは、 **[ユーザーまたはグループ**] ダイアログ ボックスの一覧に表示されない場合は、その名前を入力 (IUSR\_*コンピューター名*) 空白の下にボックスし、[**追加**] をクリックします。

6.  **[OK]** をクリックします。

