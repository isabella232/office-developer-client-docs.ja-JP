---
title: Append メソッド (ADOX Procedures)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476563"
---
# <a name="append-method-adox-procedures"></a>Append メソッド (ADOX Procedures)


**適用されます**Access 2013 |。Office 2013


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
> <P>Microsoft Jet 用 OLE DB プロバイダーを使用して、<STRONG>プロシージャ</STRONG>コレクションの<STRONG>Append</STRONG>メソッドができます<EM>コマンド</EM>パラメーターの<STRONG>プロシージャ</STRONG>ではなく<STRONG>ビュー</STRONG>を指定します。 <STRONG>View</STRONG> がデータ ソースに追加され、 <STRONG>Procedures</STRONG> コレクションに追加されます。 <STRONG>Append</STRONG> の後、 <STRONG>Procedures</STRONG> コレクションと <STRONG>Views</STRONG> コレクションが更新された場合、 <STRONG>View</STRONG> は <STRONG>Procedures</STRONG> コレクション内に存在しなくなり、 <STRONG>Views</STRONG> コレクションに表示されます。</P>


