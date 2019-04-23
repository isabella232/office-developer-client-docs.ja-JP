---
title: Open メソッド (ADO Stream)
TOCTitle: Open method (ADO Stream)
ms:assetid: fa2e6aaa-e9f5-009c-f3a0-050a00abf9b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250275(v=office.15)
ms:contentKeyID: 48548833
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a943209ce329d59fb4846ed18fd008bc45803da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288386"
---
# <a name="open-method-ado-stream"></a>Open メソッド (ADO Stream)


**適用先:** Access 2013、Office 2013


バイナリ データまたはテキスト データのストリームを操作するために [Stream](stream-object-ado.md) オブジェクトを開きます。

## <a name="syntax"></a>構文

*ストリーム*。 Open *Source*、 *Mode*、 *openoptions*、 *UserName*、 *Password*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Source* |省略可能です。 **ストリーム**のデータソースを指定する**バリアント型 (Variant** ) の値です。 *Source*には、電子メールやファイルシステムなど、既知のツリー構造内の既存のノードを指す絶対 URL 文字列を含めることができます。 url は、url キーワード ("url =*scheme*//*サーバー*/*フォルダー*") を使用して指定する必要があります。 または、 *Source*には既に開いている[record](record-object-ado.md)オブジェクトへの参照が含まれている場合があります。これにより、 **record**に関連付けられている既定のストリームが開きます。 *source*が指定されていない場合、既定では、基になるソースに関連付けられていない**ストリーム**がインスタンス化されて開きます。 URL スキームとそれに関連付けられたプロバイダーの詳細については、「[絶対 url と相対 url](absolute-and-relative-urls.md)」を参照してください。|
|*Mode* |省略可能です。結果の **Stream** に対するアクセス モード (読み取り/書き込み、読み取り専用など) を [ConnectModeEnum](connectmodeenum.md) 値で指定します。既定値は **adModeUnknown** です。アクセス モードの詳細については、「[Mode プロパティ (ADO)](mode-property-ado.md)」を参照してください。*Mode* を指定しない場合は、ソース オブジェクトから継承されます。たとえば、ソース **Record** が読み取り専用モードで開かれている場合、既定では、その **Stream** も読み取り専用モードで開かれます。|
|*OpenOptions* |省略可能です。[StreamOpenOptionsEnum](streamopenoptionsenum.md) 値を指定します。既定値は **adOpenStreamUnspecified** です。|
|*UserName* |省略可能です。必要に応じて、 **Stream** オブジェクトにアクセスするためのユーザー ID を含む、文字列型 ( **String** ) の値を指定します。|
|*Password* |省略可能です。必要に応じて、 **Stream** オブジェクトにアクセスするためのパスワードを含む、文字列型 ( **String** ) の値を指定します。|

## <a name="remarks"></a>注釈

**Record** オブジェクトをソース パラメーターとして渡した場合、その **Record** オブジェクトへのアクセスは既に有効になっているため、*UserID* パラメーターと *Password* パラメーターは使用されません。同様に、**Record** オブジェクトの [Mode](mode-property-ado.md) が、**Stream** オブジェクトに転送されます。*Source* を指定しない場合、開かれた **Stream** にはデータが含まれず、[Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) はゼロ (0) になります。**Stream** を閉じたときに、この **Stream** に書き込まれたデータが失われるのを防ぐには、[CopyTo](copyto-method-ado.md) メソッドまたは [SaveToFile](savetofile-method-ado.md) メソッドを使用して **Stream** を保存するか、またはメモリの別の場所に保存します。

*OpenOptions* 値の **adOpenStreamFromRecord** は、*Source* パラメーターの内容を、既に開かれた **Record** オブジェクトとして識別します。既定の動作では、ファイルなどのツリー構造内のノードを直接指し示す URL として *Source* を扱います。そのノードに関連付けられる既定のストリームが開かれます。

**Stream** が開かれていないときは、 **Stream** の読み取り専用プロパティをすべて読み取ることができます。 **Stream** が非同期で開かれている場合、以降のすべての操作 ( [State](state-property-ado.md) プロパティやその他の読み取り専用プロパティの確認を除く) は、 **Open** 操作が完了するまでブロックされます。

上で説明したオプションに加えて、*Source* を指定しないことにより、基になるソースに関連付けることなく、**Stream** オブジェクトのインスタンスをメモリ内に作成することができます。ストリームにデータを動的に追加するには、[Write](write-method-ado.md) または [WriteText](writetext-method-ado.md) を使用してバイナリ データまたはテキスト データを **Stream** に書き込むか、または [LoadFromFile](loadfromfile-method-ado.md) を使用してデータをファイルから読み込みます。

