---
title: TNEF によるメッセージのエンコード
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336702"
---
# <a name="encoding-a-message-with-tnef"></a>TNEF によるメッセージのエンコード

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが送信されると、トランスポートプロバイダーは、転送中にメッセージを格納するために使用されるファイルを作成できます。 次に、 [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスがファイルをラップします。 次に、トランスポートプロバイダーは、 [ITnef](itnefiunknown.md)メソッドを使用して、受信側トランスポートプロバイダーが簡単にプロパティを解読できるようにするタグ付き形式のストリームにメッセージプロパティを書き込みます。 
  
**メッセージ全体を1つのファイルで表すには**
  
1. [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトとメッセージを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡すことによって、TNEF オブジェクトを取得します。 
    
2. [imapiprop:: getproplist](imapiprop-getproplist.md)メソッドを呼び出して、メッセージに対して定義されているすべてのプロパティの一覧を取得します。 
    
3. メッセージシステムでサポートされているすべてのプロパティを除外するには、 [imapiprop](imapipropiunknown.md)メソッドを使用します。 適切なタイミングで、メッセージングシステムが必要とする形式で、これらのプロパティをメッセージングシステムに書き込みます。 
    
4. [ITnef:: addprops](itnef-addprops.md)を呼び出して、残りのプロパティ (すべての添付ファイルを含む) をエンコードします。 
    
5. 要求されたすべてのプロパティが追加された後に、メッセージを TNEF ストリームにエンコードするには、 [ITnef:: Finish](itnef-finish.md)メソッドを呼び出します。 
    
6. タグ付きメッセージテキストを取得するには、 [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出します。 このタグ付きテキストは、OLE [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスのメソッドを使用してメッセージングシステムに書き出されます。 
    
7. [IUnknown:: release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッドを呼び出して、 **ITnef**オブジェクトを解放します。 
    
**受信 TNEF メッセージを処理するには**
  
1. mapi スプーラーから mapi メッセージオブジェクトを取得し、新しい mapi メッセージにメッセージヘッダーのプロパティを書き込みます。
    
2. 受信メッセージからの TNEF データを格納する[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトを作成して初期化します。 
    
3. MAPI メッセージと[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡します。 
    
4. [ITnef:: ExtractProps](itnef-extractprops.md)メソッドを呼び出して、TNEF データ内の情報をデコードします。 
    
   > [!NOTE]
   > **ExtractProps**によってデコードされたすべてのプロパティは、受信メッセージのエンベロープからデコードされたプロパティを上書きします。 つまり、抽出された TNEF プロパティは、メッセージ内の既存のプロパティを上書きします。 
  
5. タグ付きメッセージテキストを処理するには、 [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md)を呼び出し、テキストを解析して添付ファイルの位置を復元します。 
    
6. [imapiprop:: SaveChanges](imapiprop-savechanges.md)を呼び出して、メッセージを保存します。
    
7. [IUnknown:: release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッドを呼び出して、TNEF オブジェクトを解放します。 
    

