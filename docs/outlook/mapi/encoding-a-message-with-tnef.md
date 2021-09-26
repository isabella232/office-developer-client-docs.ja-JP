---
title: TNEF によるメッセージのエンコード
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6b86d9a9-6876-4885-ae1e-8571b25b85cc
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1d45a79b9b0817e760d53327da5c5e5ef82a67e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630951"
---
# <a name="encoding-a-message-with-tnef"></a>TNEF によるメッセージのエンコード

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが送信されると、トランスポート プロバイダーは、転送中にメッセージを格納するために使用されるファイルを作成できます。 次に [、IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) インターフェイスがファイルにラップされます。 次に、トランスポート プロバイダーは [ITnef](itnefiunknown.md) メソッドを使用して、メッセージ プロパティをタグ付き形式でストリームに書き込み、受信トランスポート プロバイダーによってプロパティを簡単にデコードできます。 
  
**1 つのファイル内のメッセージ全体を表す**
  
1. IStream オブジェクトとメッセージを[OpenTnefStreamEx](opentnefstreamex.md)関数に渡して[、TNEF](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)オブジェクトを取得します。 
    
2. [IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドを呼び出して、メッセージのすべての定義済みプロパティの一覧を取得します。 
    
3. [IMAPIProp メソッドを](imapipropiunknown.md)使用して、メッセージング システムでサポートされているすべてのプロパティを除外します。 適切な時点で、メッセージング システムに必要な形式でこれらのプロパティをメッセージング システムに書き込む。 
    
4. [ITnef::AddProps](itnef-addprops.md)を呼び出して、すべての添付ファイルを含む残りのプロパティをエンコードします。 
    
5. 要求された [プロパティが追加された後、ITnef::Finish](itnef-finish.md) メソッドを呼び出して、メッセージを TNEF ストリームにエンコードします。 
    
6. タグ付 [きメッセージ テキストを取得するには、ITnef::OpenTaggedBody](itnef-opentaggedbody.md) メソッドを呼び出します。 このタグ付きテキストは、OLE IStream インターフェイスのメソッドを使用してメッセージング システム [に書き込](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) まれます。 
    
7. [IUnknown::Release メソッドを呼び](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)出して **、ITnef オブジェクトを解放** します。 
    
**受信 TNEF メッセージを処理するには**
  
1. MAPI スプーラーから MAPI メッセージ オブジェクトを取得し、新しい MAPI メッセージにメッセージ ヘッダー プロパティを書き込む。
    
2. 受信メッセージの [TNEF](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) データを含む IStream オブジェクトを作成および初期化します。 
    
3. MAPI メッセージと [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) オブジェクトを [OpenTnefStreamEx 関数に渡](opentnefstreamex.md) します。 
    
4. [ITnef::ExtractProps](itnef-extractprops.md)メソッドを呼び出して、TNEF データ内の情報をデコードします。 
    
   > [!NOTE]
   > **ExtractProps でデコードされた内容は、** 受信メッセージのエンベロープからデコードされたプロパティを上書きします。 つまり、抽出された TNEF プロパティは、メッセージ内の既存のプロパティを上書きします。 
  
5. [ITnef::OpenTaggedBody](itnef-opentaggedbody.md)を呼び出してタグ付きメッセージ テキストを処理し、テキストを解析して添付ファイルの位置を回復します。 
    
6. [IMAPIProp::SaveChanges を呼び出してメッセージを保存します](imapiprop-savechanges.md)。
    
7. [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx)メソッドを呼び出して、TNEF オブジェクトを解放します。 
    

