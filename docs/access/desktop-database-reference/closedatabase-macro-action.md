---
title: CloseDatabase マクロ アクション
TOCTitle: CloseDatabase macro action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac29cbdae8c162a992f2763530514150ca0240ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296298"
---
# <a name="closedatabase-macro-action"></a>CloseDatabase マクロ アクション


**適用先:** Access 2013、Office 2013

"CloseDatabase/データベースを閉じる" アクションを使用すると、カレント データベースを閉じることができます。

## <a name="setting"></a>Setting

"CloseDatabase/データベースを閉じる" アクションには、引数はありません。

## <a name="remarks"></a>注釈

  - マクロの中で "CloseDatabase/データベースを閉じる" アクションより後に設定されたアクションは実行されません。

  - このアクションの動作は、[**ファイル**] タブをクリックし、[**データベースを閉じる**] をクリックした場合と同じです。 If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.

  - To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.

