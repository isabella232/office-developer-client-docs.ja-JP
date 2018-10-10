---
title: "'CloseDatabase/データベースを閉じる' マクロ アクション"
TOCTitle: CloseDatabase Macro Action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d2c60d53b6798d3385bdcfb17669134a04ba6195
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479530"
---
# <a name="closedatabase-macro-action"></a>"CloseDatabase/データベースを閉じる" マクロ アクション


**適用されます**Access 2013 |。Office 2013

**CloseDatabase**アクションを使用すると、現在のデータベースを閉じます。

## <a name="setting"></a>設定値

**CloseDatabase**アクションの引数ではありません。

## <a name="remarks"></a>解説

  - アクセスでは、次のマクロで**CloseDatabase**アクションのすべてのアクションは実行されません。

  - この操作には、として、[**ファイル**] タブをクリックし、**データベースを閉じる**をクリックし、同じ効果があります。 未保存のオブジェクトは、開いている場合**CloseDatabase**アクションを実行すると、ダイアログ ボックスが表示、**データベースを閉じる**をクリックすると表示されるものと同じです。

  - Visual Basic for Applications (VBA) モジュールで**CloseDatabase**アクションを実行するには、 **DoCmd**オブジェクトの**CloseDatabase**メソッドを使用します。

