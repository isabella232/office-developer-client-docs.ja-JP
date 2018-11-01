---
title: "'CloseDatabase/データベースを閉じる' マクロ アクション"
TOCTitle: CloseDatabase Macro Action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 42ba5925c35081f612bd4a81b49f3c2b16cf61dd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876639"
---
# <a name="closedatabase-macro-action"></a>"CloseDatabase/データベースを閉じる" マクロ アクション


**適用されます**Access 2013、Office 2013。

**CloseDatabase**アクションを使用すると、現在のデータベースを閉じます。

## <a name="setting"></a>設定値

**CloseDatabase**アクションの引数ではありません。

## <a name="remarks"></a>解説

  - アクセスでは、次のマクロで**CloseDatabase**アクションのすべてのアクションは実行されません。

  - この操作には、として、[**ファイル**] タブをクリックし、**データベースを閉じる**をクリックし、同じ効果があります。 未保存のオブジェクトは、開いている場合**CloseDatabase**アクションを実行すると、ダイアログ ボックスが表示、**データベースを閉じる**をクリックすると表示されるものと同じです。

  - Visual Basic for Applications (VBA) モジュールで**CloseDatabase**アクションを実行するには、 **DoCmd**オブジェクトの**CloseDatabase**メソッドを使用します。

