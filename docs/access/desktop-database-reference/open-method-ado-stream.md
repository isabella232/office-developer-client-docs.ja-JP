---
title: Open メソッド (ADO Stream)
TOCTitle: Open Method (ADO Stream)
ms:assetid: fa2e6aaa-e9f5-009c-f3a0-050a00abf9b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250275(v=office.15)
ms:contentKeyID: 48548833
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac01f67bb18ea15959f4b5c09dbe4037da8010bc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883240"
---
# <a name="open-method-ado-stream"></a>Open メソッド (ADO Stream)


**適用されます**Access 2013、Office 2013。


バイナリ データまたはテキスト データのストリームを操作するために [Stream](stream-object-ado.md) オブジェクトを開きます。

## <a name="syntax"></a>構文

*ストリーム*。 *ソース*、*モード*、 *OpenOptions*、*ユーザー名*、*パスワード*を開く

## <a name="parameters"></a>パラメーター

  - *Source*

  - 省略可能です。 **ストリーム**のデータのソースを指定する**バリアント型**の値です。 *ソース*に、電子メールまたはファイル システムのように、既知のツリー構造内の既存のノードを指す絶対 URL 文字列が含まれている可能性があります。 URL キーワードを使用して URL を指定する必要があります (「URL://*サーバー*の*設定*を =/*フォルダー*"). 代わりに、*ソース*には、**レコード**に関連付けられた既定ストリームを開きの既に開いている[Record](record-object-ado.md)オブジェクトへの参照が含まれて可能性があります。 *ソース*が指定されていない場合、**ストリーム**は、既定でない基になるソースに関連付けられています。 URL スキームと、関連付けられているプロバイダーの詳細については、[絶対パスと相対 Url](absolute-and-relative-urls.md)を参照してください。

  - *Mode*

  - 省略可能です。 結果の [Stream](connectmodeenum.md) に対するアクセス モード (読み取り/書き込み、読み取り専用など) を **ConnectModeEnum** 値で指定します。 既定値は **adModeUnknown** です。 アクセス モードの詳細については、「 [Mode プロパティ (ADO)](mode-property-ado.md)」を参照してください。 *モード*を指定しない場合は、ソース オブジェクトによって継承されます。 たとえば、ソース **Record** が読み取り専用モードで開かれている場合、既定では、その **Stream** も読み取り専用モードで開かれます。

  - *OpenOptions*

  - 省略可能です。[StreamOpenOptionsEnum](streamopenoptionsenum.md) 値を指定します。既定値は **adOpenStreamUnspecified** です。

  - *UserName*

  - 省略可能です。必要に応じて、 **Stream** オブジェクトにアクセスするためのユーザー ID を含む、文字列型 ( **String** ) の値を指定します。

  - *Password*

  - 省略可能です。必要に応じて、 **Stream** オブジェクトにアクセスするためのパスワードを含む、文字列型 ( **String** ) の値を指定します。

## <a name="remarks"></a>解説

**Record**オブジェクトへのアクセスが用意されているため、ソース パラメーターは、*ユーザー Id*と*パスワード*のパラメーターとしての**Record**オブジェクトが渡されるときは使用されません。 同様に、 **Record**オブジェクトの[モード](mode-property-ado.md)は、**ストリーム**オブジェクトに転送されます。*ソース*が指定されていない、開かれている**ストリーム**はデータが含まれていないと、[サイズ](https://msdn.microsoft.com/library/jj250128\(v=office.15\))はゼロ (0)。 **ストリーム**が閉じているときに、この**ストリーム**に書き込まれるすべてのデータが失われるを避けるためには、**ストリーム**を付けて、 [CopyTo](copyto-method-ado.md)メソッドまたは[SaveToFile](savetofile-method-ado.md)メソッド、またはメモリの別の場所に保存します。

*OpenOptions*値の**adOpenStreamFromRecord**は、 *Source*パラメーターを既に開いている**レコード**オブジェクトの内容を識別します。 既定の動作では、ファイルなどのツリー構造内のノードを直接指し示す URL として*Source*を扱います。 そのノードに関連付けられる既定のストリームが開かれます。

**Stream** が開かれていないときは、 **Stream** の読み取り専用プロパティをすべて読み取ることができます。 **Stream** が非同期で開かれている場合、以降のすべての操作 ( [State](state-property-ado.md) プロパティやその他の読み取り専用プロパティの確認を除く) は、 **Open** 操作が完了するまでブロックされます。

上で説明したオプションに加えて、*Source* を指定しないことにより、基になるソースに関連付けることなく、**Stream** オブジェクトのインスタンスをメモリ内に作成することができます。ストリームにデータを動的に追加するには、[Write](write-method-ado.md) または [WriteText](writetext-method-ado.md) を使用してバイナリ データまたはテキスト データを **Stream** に書き込むか、または [LoadFromFile](loadfromfile-method-ado.md) を使用してデータをファイルから読み込みます。

