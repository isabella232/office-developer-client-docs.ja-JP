---
title: Append メソッド (ADOX Views)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477944"
---
# <a name="append-method-adox-views"></a>Append メソッド (ADOX Views)


**適用されます**Access 2013 |。Office 2013


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
> <P>Microsoft Jet 用 OLE DB プロバイダーを使用して、 <STRONG>Views</STRONG>コレクションの<STRONG>Append</STRONG>メソッドができます<EM>コマンド</EM>パラメーターの<STRONG>表示</STRONG>ではなく、<STRONG>プロシージャ</STRONG>を指定します。 <STRONG>Procedure</STRONG> がデータ ソースに追加され、 <STRONG>Views</STRONG> コレクションに追加されます。 <STRONG>Append</STRONG> の後、 <STRONG>Procedures</STRONG> コレクションと <STRONG>Views</STRONG> コレクションが更新された場合、 <STRONG>Procedure</STRONG> は <STRONG>Views</STRONG> コレクション内に存在しなくなり、 <STRONG>Procedures</STRONG> コレクションに表示されます。</P>


