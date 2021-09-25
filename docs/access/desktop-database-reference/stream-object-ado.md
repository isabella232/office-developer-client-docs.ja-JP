---
title: Stream オブジェクト (ADO)
TOCTitle: Stream object (ADO)
ms:assetid: d49b1514-e0b4-0aca-d5c2-8266f3f4fe65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250065(v=office.15)
ms:contentKeyID: 48547945
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6357a0f8ce0544294c54345bd5200b10b3fc95c3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580756"
---
# <a name="stream-object-ado"></a>Stream オブジェクト (ADO)


**適用先:** Access 2013、Office 2013

バイナリ データまたはテキストのストリームを表します。

## <a name="remarks"></a>注釈

ファイル システムや電子メール システムなどのツリー構造の階層では、 [レコード](record-object-ado.md) には、ファイルまたは電子メールの内容を含む既定のバイナリ ストリームのビットが関連付けられている場合があります。 これらのデータ ストリームを格納したフィールドまたはレコードは、 **Stream** オブジェクトを使用して操作できます。 **Stream** オブジェクトは次の方法で取得できます。

  - バイナリ データまたはテキスト データを格納したオブジェクト (通常はファイル) を指定する URL で取得します。このようなオブジェクトには、単純なドキュメント、構造ドキュメントを表す **Record** オブジェクト、またはフォルダーがあります。

  - **Record** オブジェクトに関連付けられた既定の **Stream** オブジェクトを開いて取得します。 **Record** オブジェクトが開いているときにその **Record** オブジェクトに関連付けられた既定のストリームを取得すると、ストリームを開くときに起こるラウンドトリップを避けることができます。

  - **Stream** オブジェクトをインスタンス作成して取得します。このような **Stream** オブジェクトは、アプリケーション用のデータの保存に利用できます。URL に関連付けられた **Stream** オブジェクト、または **Record** オブジェクトの既定の **Stream** オブジェクトとは異なり、インスタンス作成した **Stream** オブジェクトは、既定では基になるソースに関連付けられていません。

**Stream** オブジェクトのメソッドとプロパティを使用すると、次の操作を実行できます。

  - **Open** メソッドを使用して、 **Record** または URL から [Stream](open-method-ado-stream.md) オブジェクトを開くことができます。

  - **Close** メソッドを使用して、 [Stream](close-method-ado.md) を閉じることができます。

  - **Write** メソッドまたは [WriteText](write-method-ado.md) メソッドを使用して、バイトまたはテキストを [Stream](writetext-method-ado.md) に入力できます。

  - **Read** メソッドまたは [ReadText](read-method-ado.md) メソッドを使用して、 [Stream](readtext-method-ado.md) からバイトを読み取ることができます。

  - **Flush** メソッドを使用して、ADO バッファーにある [Stream](flush-method-ado.md) データを基になるオブジェクトに書き込むことができます。

  - **CopyTo** メソッドを使用して、 **Stream** の内容を別の [Stream](copyto-method-ado.md) にコピーできます。

  - [SkipLine](skipline-method-ado.md) メソッドおよび [LineSeparator](lineseparator-property-ado.md) プロパティを使用して、ソース ファイルから行を読み取る方法を制御できます。

  - [EOS](eos-property-ado.md) プロパティおよび [SetEOS](seteos-method-ado.md) メソッドを使用して、ストリーム位置の末尾を設定できます。

  - [SaveToFile](savetofile-method-ado.md) メソッドおよび [LoadFromFile](loadfromfile-method-ado.md) メソッドを使用して、ファイル内のデータを保存および復元できます。

  - **Charset** プロパティを使用して、 [Stream](charset-property-ado.md) の保存に使用する文字セットを指定できます。

  - **Cancel** メソッドを使用して、非同期 [Stream](cancel-method-ado.md) 操作を停止できます。

  - **Size** プロパティを使用して、 [Stream](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) 内のバイト数を設定できます。

  - **Position** プロパティを使用して、 [Stream](position-property-ado.md) 内の現在の位置を制御できます。

  - **Type** プロパティを使用して、 [Stream](type-property-ado-stream.md) 内のデータ型を設定できます。

  - **State** プロパティを使用して、 [Stream](state-property-ado.md) の現在の状態 (開いている、閉じている、または実行中) を設定できます。

  - **Mode** プロパティを使用して、 [Stream](mode-property-ado.md) のアクセス モードを指定できます。

> [!NOTE]
> [!メモ] http スキームを使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。 詳細については、「絶対 URL と [相対 URL」を参照してください](absolute-and-relative-urls.md)。


