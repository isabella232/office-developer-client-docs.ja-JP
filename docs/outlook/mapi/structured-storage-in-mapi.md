---
title: MAPI での構造化ストレージ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: f58fa70e98841db5507323a63737f1df6c1b7a6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411751"
---
# <a name="structured-storage-in-mapi"></a>MAPI での構造化ストレージ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
構造化ストレージとは、COM で導入された記憶域の階層構造を意味します。 構造化ストレージ環境では、ストレージは2つまたは3つの種類のオブジェクトに編成されます。 
  
- Stream オブジェクト
    
- bytes オブジェクトをロックする
    
- ストレージオブジェクト
    
Stream および lock バイトは、データに直接アクセスする下位レベルのオブジェクトです。 Stream オブジェクトは、データのバイトを読み取り、書き込み、配置、およびコピーするためのメソッドを定義する**IStream**インターフェイスを実装します。 Lock bytes オブジェクトは、バイト配列を使用してデータにアクセスするために、別の COM インターフェイス**ILockBytes**を実装します。 通常、バイト配列は、基になるストレージへのカスタマイズアクセスを提供するために使用されます。
  
ストレージオブジェクトは、stream または lock bytes オブジェクトに重なっています。これらのオブジェクトには、その他のストレージオブジェクトだけでなく、1つ以上のオブジェクトを含めることができます。 Storage オブジェクトは、ネストされたオブジェクトを作成、アクセス、および維持するためのメソッドを定義する**IStorage**インターフェイスを実装しています。 
  
**IStream**、 **ILockBytes**、および**IStorage**は mapi インターフェイスではなく com インターフェイスなので、これらのメソッドは mapi の値ではなく com のエラー値を返します。 これらのインターフェイスでメソッドを呼び出すクライアントおよびサービスプロバイダーは、API 関数**mapstoragescode**を使用してこれらの値を MAPI エラー値に変換する必要があります。 詳細については、「 [mapstoragescode](mapstoragescode.md)」を参照してください。
  
クライアントおよびサービスプロバイダーは構造化ストレージを使用して、 **imapiprop**メソッド (通常は長い文字列およびバイナリプロパティ) で保持するには大きすぎるプロパティを処理します。 クライアントまたはサービスプロバイダーがアクセスする一般的な方法の1つは、 [imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出して、インターフェイス識別子として**IStream**または**IStorage**を指定することです。 たとえば、クライアントは、 **PR_ATTACH_DATA_BIN**をプロパティタグとして、IID_IStream として、メッセージ内のバイナリ添付ファイルにアクセスするためのインターフェイス識別子として、 **openproperty**を呼び出します。 
  
クライアントおよびサービスプロバイダーは、独自の stream オブジェクトと storage オブジェクトを実装したり、API 関数を呼び出したりして、MAPI または COM によって提供される実装にアクセスできます。 提供される実装はほとんどの目的に対応しているため、クライアントおよびサービスプロバイダーが独自に作成する必要はまれです。 
  
クライアントが MAPI オブジェクトの**openproperty**を呼び出して、ストレージオブジェクト経由でそのプロパティの1つにアクセスすると、通常、サービスプロバイダーはそのストレージオブジェクトを直接モードで開きます。 ただし、これは必要な動作ではなく一般的になります。 クライアントは、サービスプロバイダーによって開かれた、または作成されたすべてのストレージオブジェクトが処理され、 **IStorage:: Commit**を呼び出す必要があると想定する必要があります。 また、ストレージオブジェクトへの変更は、MAPI オブジェクトを保存する最終**コミット**後に、 **imapiprop:: SaveChanges**を呼び出すまで永続的には行われないことに注意してください。 詳細については、「 [imapiprop:: SaveChanges](imapiprop-savechanges.md)」を参照してください。
  
MAPI と COM には、ストレージおよび stream オブジェクトを定義したりアクセスしたりするための複数の API 関数が用意されています。 次の表では、一般的に使用される関数について説明します。
  
**ストレージおよび Stream オブジェクトにアクセスするための関数**

|**関数**|**説明**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |stream または lock バイトオブジェクトにアクセスするためのストレージオブジェクトを作成します。  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |ストレージオブジェクトにアクセスするための message オブジェクトを作成します。  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |ファイルにアクセスするための stream オブジェクトを作成します。  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |メッセージのリッチテキストを保持する圧縮または圧縮されていないバージョンのストリームを含む stream オブジェクトを作成します。  <br/> |
   
 **指定したサブストレージのストリームの名前を取得するには**
  
1. サブストレージの**IStorage:: enumelements**メソッドを呼び出して、 **IEnumSTATSTG**インターフェイスを取得します。 
    
2. **IEnumSTATSTG:: 次**のように、同時にできるだけ多くの**STATSTG**構造を使用して、次のように呼び出します。 一度に100を要求した場合、**次**に、通常は、実際に取得された_pceltfetched_セットの内容を使用して S_FALSE を返します。 
    
3. STGTY_STREAM を使用してフラグが設定されている**STATSTG**構造を確認します。 
    
4. _pwcsName_パラメーターを解放します。 
    
 **既存の stream または lock bytes オブジェクトにアクセスするためのストレージオブジェクトを作成するには**
  
- クライアントは、 [hristoragefromstream](hristoragefromstream.md)を呼び出します。 
    
 **既存のストレージオブジェクトにアクセスするためのメッセージオブジェクトを作成するには**
  
- サービスプロバイダーとクライアントは[OpenIMsgOnIStg](openimsgonistg.md)を呼び出します。 作成されるメッセージオブジェクトは、通常、メッセージストアプロバイダーによって作成されるメッセージオブジェクトと異なります。これは、 **IMessage:: submitmessage**のような[IMessage: imapiprop](imessageimapiprop.md)のインターフェイスメソッドをすべてサポートしているわけではありません。 **OpenIMsgOnIStg**へのオプションの入力パラメーターは、 [msgcallrelease](msgcallrelease.md)プロトタイプに準拠するコールバック関数です。 この関数は、メッセージの参照カウントが0に達したときに、新しい message オブジェクトによって呼び出されます。 **msgcallrelease**関数の実装は、新しいメッセージが完全に削除される前に、最終的な処理を実行するために役立ちます。 
    
[openstreamonfile](openstreamonfile.md)は、ファイルの読み取りおよび書き込みを行うストリームを作成するので、通常はファイル添付を格納するために使用されます。 プロパティタグとして**PR_ATTACH_DATA_BIN**を持つ**openproperty**は、バイナリ添付ファイルデータを格納するストリームを作成します。 
  
 **リッチテキスト形式のメッセージテキストを含むストリームを圧縮または圧縮解除するには**
  
- クライアントは[WrapCompressedRTFStream](wrapcompressedrtfstream.md)を呼び出します。 **WrapCompressedRTFStream**は、RTF ストリームをラップするストリームを作成します。 ラッパーストリームは、すべての**IStream**メソッドを実装するわけではありません。次のメソッドは除外されます。 **Seek**、 **SetSize**、 **Revert**、 **lockregion**、 **UnlockRegion**、 **Stat**、および**Clone**。 これは、 **WrapCompressedRTFStream**によって作成された stream オブジェクトが**SetSize**または**Stat**をサポートしていないためです。サイズを拡張または取得する簡単な方法はありません。 最適な方法は、適切なバッファーサイズを選択し、ループで読み取りまたは書き込みを行うことです。
    
> [!NOTE]
> COM には、 **enumelements**メソッドから**IEnumSTATSTG**オブジェクトを返すバイト配列に基づいたストレージオブジェクトの実装があり、問題があります。 特に、 **QueryInterface**メソッドは正しく動作しません。 COM 実装を使用して独自のストレージオブジェクトを実装するサービスプロバイダーは、元の**IEnumSTATSTG**メソッドに呼び出しを転送し、独自の AddRef を実装する**IEnumSTATSTG**オブジェクトのシンラッパーを作成する必要があります。 ****、 **Release**、 **QueryInterface**、および**Clone**の各メソッドを示します。 
  

