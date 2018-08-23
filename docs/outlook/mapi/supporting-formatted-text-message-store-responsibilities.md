---
title: 書式付きのテキスト ・ メッセージ ・ ストアの役割をサポートしています。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 301ebbf8e7a3e2a2deb303af5b198fd11511d495
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804026"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>書式付きテキストのサポート: メッセージ ストアの責任

  
  
**適用対象**: Outlook 
  
メッセージ ストア プロバイダーで書式設定されたテキストを格納するかどうかは、RTF を認識されている場合、リッチ テキスト形式式 (RTF)、HTML テキストを処理できるかどうかを公開する**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを使用して、圧縮または非圧縮形式です。 メッセージ ストア プロバイダーは、ある RTF に対応して、STORE_RTF_OK ビットを設定することによって、格納していること、書式設定されたテキスト、未圧縮の形式で STORE_UNCOMPRESSED_RTF ビットを設定することによってを示します。 メッセージ ストア プロバイダーは、STORE_HTML_OK ビットを設定することによって HTML に対応していることを示します。
  
Rtf 形式に対応していないクライアントがメッセージ ・ ストアが RTF をサポートしているかどうかを決定するビットの STORE_RTF_OK をチェックするのに重要なは、クライアントに rtf 形式に対応していない店舗の書式設定されたテキストの書式と注意を払う必要はありません。 
  
すべてのメッセージ ストアには、RTF に対応していないクライアントをサポートする必要があります。 RTF に対応していないメッセージ ストアは、せずにクライアントが**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) に変更された場合に、メッセージの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの呼び出し中の**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティを削除する必要があります。**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) または**PR_RTF_IN_SYNC**のいずれかを更新しています。 **PR_RTF_IN_SYNC**を削除すると、 **PR_RTF_COMPRESSED**プロパティは、次に、rtf 形式に対応したクライアント[へ](rtfsync.md)の呼び出しに**PR_BODY**プロパティの再計算が発生します。 
  
RTF に対応していないメッセージ ストアがほとんどないによって与えられます。 メッセージ テキスト クライアントです。要求を計算する必要があります。 この計算で時間とコストがあるため、クライアントは、可能な限り**PR_RTF_COMPRESSED**を使用してください。 **PR_BODY**プロパティを計算するには、メッセージ ストア プロバイダーする必要があります**PR_RTF_COMPRESSED**プロパティの内容を圧縮解除をリッチ テキストの書式設定を削除できます。 **PR_RTF_COMPRESSED**プロパティをサポートしていないクライアントは、すべてのメッセージに対して実行するには、この計算を必要とします。 
  
メッセージ ・ ストア プロバイダーの実装に**PR_BODY**が除外されている場合は、内容のないメッセージを作成するリスクを実行する**IMAPISupport::DoCopyProps**または**IMAPISupport::DoCopyTo**メソッドを使用してメッセージをコピーする場合プロパティ**PR_RTF_COMPRESSED**に依存しているとします。 破損していること、 **PR_RTF_COMPRESSED**プロパティ内のデータのことができます。 コピー操作でこれらのメッセージ コンテンツ プロパティのいずれかを除外するには、前に、破損のとおり確認します。 
  
1. **PR_RTF_COMPRESSED**の値が圧縮された RTF を超えていない場合、プロパティが壊れています。 
    
2. Rtf 形式のヘッダー内の魔法の値が、 _dwMagicCompressedRTF_または_dwMagicUncompressedRTF_プロパティではない場合は、壊れています。
    
メッセージは、 **PR_RTF_COMPRESSED**破損のチェックを実装することを心配する必要はありませんメソッドが必要なサポートを使用して、プロバイダーを格納します。MAPI では、適切なプロパティが存在し、有効なことを保証します。 
  
メッセージ ストア プロバイダーを実装できます。 RTF のサポートの 3 つの異なるレベルします。MAPI では、rtf 形式に対応したメッセージ ストア プロバイダーが中間または高いレベルでのサポートを実装することをお勧めします。 すべて RTF に対応していないメッセージ ストア プロバイダー **PR_BODY**を生成する送信メッセージに、 **PR_RTF_COMPRESSED**に含まれるデータを処理し、テキストおよび受信メッセージの書式設定を同期する呼び出しを**行う**。 
  
これら 3 つのレベル間の相違点については、次の表で説明します。 
  
|**レベルのサポート**|**説明**|
|:-----|:-----|
|低  <br/> |メッセージでは、メッセージに変更を保存するたびに、プロバイダー**へ**の呼び出しを格納し、それを設定するのには、必要とするクライアントの代わりに**PR_RTF_COMPRESSED**から**PR_BODY**プロパティのデータを抽出します。 **PR_BODY**と**PR_RTF_COMPRESSED**の両方が格納されます。  <br/> |
|中央揃え  <br/> |メッセージは、 **PR_RTF_COMPRESSED**プロパティのみ、コンピューティングの**PR_BODY**と必要なプロバイダーのストアを格納します。  <br/> |
|高  <br/> |**PR_BODY**または補助の rtf 形式のプロパティのどちらも、メッセージはストアのプロバイダーを格納します。 **** メッセージのテキストが変更され、書式設定は変更されない場合、または新しいメッセージがダウンロードされると、トランスポート プロバイダーによって呼び出されます。  <br/> |
   

