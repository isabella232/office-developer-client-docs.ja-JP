---
title: Append メソッド (ADOX Procedures)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f086a24ba7069aae02f3001fae9bfe7a360297a9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558990"
---
# <a name="append-method-adox-procedures"></a>Append メソッド (ADOX Procedures)

**適用先:** Access 2013、Office 2013

新しい [Procedure](procedure-object-adox.md) オブジェクトを [Procedures](procedures-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*プロシージャ*.Append *Name*, *Command*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*名前* |新たに作成して追加するプロシージャの名前を示す文字列型 ( **String** ) の値を指定します。|
|*Command* |新たに作成して追加するプロシージャを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。|

## <a name="remarks"></a>注釈

**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいプロシージャを作成します。

ユーザーが指定したコマンド テキストがプロシージャではなくビューを表す場合、動作は使用しているプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。

> [!NOTE]
> OLE DB Provider for Microsoft Jet を使用しているとき、**Procedures** コレクションの **Append** メソッドによって **Procedure** ではなく **View** を *Command* パラメーターに指定することができます。**View** がデータ ソースに追加され、**Procedures** コレクションに追加されます。**Append** の後、**Procedures** コレクションと **Views** コレクションが更新された場合、**View** は **Procedures** コレクション内に存在しなくなり、**Views** コレクションに表示されます。


