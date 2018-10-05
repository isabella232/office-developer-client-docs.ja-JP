---
title: TNEF メッセージをエンコードします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: cdaa03cfbc0bbd0fcf6a320ecf8fae9f372d5781
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382527"
---
# <a name="encoding-a-message-with-tnef"></a>TNEF メッセージをエンコードします。

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが送信されると、トランスポート プロバイダーは、転送中にメッセージを格納するために使用されるファイルを作成できます。 次に、 [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスは、ファイルを囲みます。 トランスポート プロバイダーは、ストリームに書き込むメッセージのプロパティ、受信側のトランスポート プロバイダーが簡単にデコードするのににはプロパティを有効にするタグ付きの形式で、 [ITnef](itnefiunknown.md)メソッドを使用します。 
  
**1 つのファイル全体のメッセージを表す**
  
1. [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトとメッセージを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡すことによって TNEF オブジェクトを取得します。 
    
2. [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを呼び出して、メッセージのすべての定義済みプロパティの一覧を取得します。 
    
3. [IMAPIProp](imapipropiunknown.md)メソッドを使用すると、メッセージング システムでサポートされているすべてのプロパティを除外できます。 適切なタイミングでは、メッセージング システムに必要な形式でのメッセージング システムにこれらのプロパティを記述します。 
    
4. すべての添付ファイルを含め、他のプロパティをエンコードするために[ITnef::AddProps](itnef-addprops.md)を呼び出します。 
    
5. 要求されたすべてのプロパティを追加した後は、TNEF ストリームにメッセージをエンコードするために[ITnef::Finish](itnef-finish.md)メソッドを呼び出します。 
    
6. タグ付きのメッセージ テキストを取得する[ITnef::OpenTaggedBody](itnef-opentaggedbody.md)メソッドを呼び出します。 このタグ付きテキストは、OLE の[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスからメソッドを使用してメッセージング システムに書き出されます。 
    
7. **ITnef**オブジェクトを解放する[が](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッドを呼び出します。 
    
**TNEF メッセージの受信を処理するのには**
  
1. MAPI スプーラーから MAPI メッセージ オブジェクトを取得し、新しい MAPI メッセージにメッセージのヘッダー プロパティを記述します。
    
2. 作成し、受信メッセージの TNEF データが含まれている[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトを初期化します。 
    
3. MAPI メッセージと[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡します。 
    
4. [ITnef::ExtractProps](itnef-extractprops.md)メソッドを呼び出すことによって TNEF データ内の情報をデコードします。 
    
   > [!NOTE]
   > **ExtractProps**でデコードされたものは、受信メッセージのエンベロープからデコードされたプロパティで上書きされます。 TNEF プロパティの抽出されたメッセージでは、既存のプロパティが上書きされます。 
  
5. [ITnef::OpenTaggedBody](itnef-opentaggedbody.md)を呼び出すことによってタグ付けされたメッセージのテキストを処理し、添付ファイルの位置を回復するのにはテキストを解析します。 
    
6. [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出すことによって、メッセージを保存します。
    
7. [](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッドを呼び出すことによって TNEF オブジェクトを解放します。 
    

