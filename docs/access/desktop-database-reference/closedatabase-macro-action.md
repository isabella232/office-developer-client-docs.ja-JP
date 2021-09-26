---
title: CloseDatabase マクロ アクション
TOCTitle: CloseDatabase macro action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f08200d2037ab09c8c9aee4ebcc8a98ae228ca2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622495"
---
# <a name="closedatabase-macro-action"></a>CloseDatabase マクロ アクション


**適用先**: Access 2013、Office 2013

"CloseDatabase/データベースを閉じる" アクションを使用すると、カレント データベースを閉じることができます。

## <a name="setting"></a>設定

"CloseDatabase/データベースを閉じる" アクションには、引数はありません。

## <a name="remarks"></a>注釈

  - マクロの中で "CloseDatabase/データベースを閉じる" アクションより後に設定されたアクションは実行されません。

  - このアクションは、[ファイル] タブをクリックし、[データベースの閉じる] をクリックするのと **同じ効果があります**。 If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.

  - To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.

