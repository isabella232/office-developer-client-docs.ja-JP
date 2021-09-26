---
title: Append メソッド (ADOX Views)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b6dd5ffc50e487cb00022fdd96708bea713ed006
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607326"
---
# <a name="append-method-adox-views"></a>Append メソッド (ADOX Views)

**適用先**: Access 2013、Office 2013

新しい [View](view-object-adox.md) オブジェクトを作成して [Views](views-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*ビュー*.Append *Name*, *Command*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*名前* |作成するビューの名前を示す文字列型 ( **String** ) の値を指定します。|
|*Command* |作成するビューを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。|

## <a name="remarks"></a>注釈

**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいビューを作成します。

ユーザーが指定したコマンド テキストがビューではなくプロシージャを表す場合、動作はプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。

> [!NOTE]
> OLE DB Provider for Microsoft Jet を使用しているとき、**Views** コレクションの **Append** メソッドによって **View** ではなく **Procedure** を *Command* パラメーターに指定することができます。**Procedure** がデータ ソースに追加され、**Views** コレクションに追加されます。**Append** の後、**Procedures** コレクションと **Views** コレクションが更新された場合、**Procedure** は **Views** コレクション内に存在しなくなり、**Procedures** コレクションに表示されます。


