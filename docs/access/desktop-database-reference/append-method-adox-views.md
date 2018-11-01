---
title: Append メソッド (ADOX Views)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 706ab2607f7f169b9b731f9ac81409bf1ac97230
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888210"
---
# <a name="append-method-adox-views"></a>Append メソッド (ADOX Views)


**適用されます**Access 2013、Office 2013。


新しい [View](view-object-adox.md) オブジェクトを作成して [Views](views-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*ビュー*です。*名*、*コマンド*を追加します。

## <a name="parameters"></a>パラメーター

  - *Name*

  - 作成するビューの名前を示す文字列型 ( **String** ) の値を指定します。

  - *Command*

  - 作成するビューを表す ADO の [Command](command-object-ado.md) オブジェクトを指定します。

## <a name="remarks"></a>解説

**Command** オブジェクトで指定された名前および属性を持つデータ ソースに新しいビューを作成します。

ユーザーが指定したコマンド テキストがビューではなくプロシージャを表す場合、動作はプロバイダーによって異なります。プロバイダーが永続的なコマンドをサポートしていない場合、 **Append** は失敗します。


> [!NOTE]
> Microsoft Jet 用 OLE DB プロバイダーを使用して、 **Views**コレクションの**Append**メソッドができます*コマンド*パラメーターの**表示**ではなく、**プロシージャ**を指定します。 **Procedure** がデータ ソースに追加され、 **Views** コレクションに追加されます。 **Append** の後、 **Procedures** コレクションと **Views** コレクションが更新された場合、 **Procedure** は **Views** コレクション内に存在しなくなり、 **Procedures** コレクションに表示されます。


