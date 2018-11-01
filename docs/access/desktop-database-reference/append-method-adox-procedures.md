---
title: Append メソッド (ADOX Procedures)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ef11c9d45cc5b34b5ef7b1cf762dfd6f3e4c1d64
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873048"
---
# <a name="append-method-adox-procedures"></a>Append メソッド (ADOX Procedures)


**適用されます**Access 2013、Office 2013。


新しい [Procedure](procedure-object-adox.md) オブジェクトを [Procedures](procedures-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*プロシージャ*です。*名*、*コマンド*を追加します。

## <a name="parameters"></a>パラメーター

  - *Name*

  - 新たに作成して追加するプロシージャの名前を示す文字列型 ( **String** ) の値を指定します。

  - *Command*

  - 新たに作成して追加するプロシージャを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。

## <a name="remarks"></a>解説

**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいプロシージャを作成します。

ユーザーが指定したコマンド テキストがプロシージャではなくビューを表す場合、動作は使用しているプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。


> [!NOTE]
> Microsoft Jet 用 OLE DB プロバイダーを使用して、**プロシージャ**コレクションの**Append**メソッドができます*コマンド*パラメーターの**プロシージャ**ではなく**ビュー**を指定します。 **View** がデータ ソースに追加され、 **Procedures** コレクションに追加されます。 **Append** の後、 **Procedures** コレクションと **Views** コレクションが更新された場合、 **View** は **Procedures** コレクション内に存在しなくなり、 **Views** コレクションに表示されます。


