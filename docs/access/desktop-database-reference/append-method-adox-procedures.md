---
title: Append メソッド (ADOX Procedures)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2de9dc7d8dccfc4107dbd802c4013ac794acf61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297082"
---
# <a name="append-method-adox-procedures"></a>Append メソッド (ADOX Procedures)

**適用先:** Access 2013、Office 2013

新しい [Procedure](procedure-object-adox.md) オブジェクトを [Procedures](procedures-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*手順*。Append*Name*, *Command*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Name* |新たに作成して追加するプロシージャの名前を示す文字列型 ( **String** ) の値を指定します。|
|*Command* |新たに作成して追加するプロシージャを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。|

## <a name="remarks"></a>注釈

**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいプロシージャを作成します。

ユーザーが指定したコマンド テキストがプロシージャではなくビューを表す場合、動作は使用しているプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。

> [!NOTE]
> OLE DB Provider for Microsoft Jet を使用しているとき、**Procedures** コレクションの **Append** メソッドによって **Procedure** ではなく **View** を *Command* パラメーターに指定することができます。**View** がデータ ソースに追加され、**Procedures** コレクションに追加されます。**Append** の後、**Procedures** コレクションと **Views** コレクションが更新された場合、**View** は **Procedures** コレクション内に存在しなくなり、**Views** コレクションに表示されます。


