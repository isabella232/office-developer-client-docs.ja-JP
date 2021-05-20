---
title: 送信メッセージの書式設定されたテキストのサポート クライアントの責任
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7238b1a9-01ed-46a0-a625-26763323317d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 01d5ae3fd06d570e15336fad9538f01e586cd0f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431604"
---
# <a name="supporting-formatted-text-in-outgoing-messages-client-responsibilities"></a>送信メッセージでの書式設定されたテキストのサポート: クライアントの責任

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント アプリケーションは **、PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティ **、PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティ、または送信メッセージの **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) プロパティを設定します。 プレーン テキスト セットのみをサポートするクライアントは、PR_BODY **プロパティのみです** 。 リッチ テキスト形式 (RTF) 対応のクライアントは、使用するメッセージ ストア プロバイダーに応じて、PR_BODY プロパティと **PR_RTF_COMPRESSED** プロパティの両方を設定するか、PR_RTF_COMPRESSED のみを設定できます。  HTML 対応のクライアントは、PR_HTMLプロパティ **を設定** します。 
  
クライアントは、メッセージ ストアの PR_STORE_SUPPORT_MASK **(** [PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティをチェックして、ストアが RTF をサポートするかどうかを判断することが重要です。 メッセージ ストアが RTF 対応ではない場合、RTF 対応クライアントは、送信メッセージごとに PR_BODYプロパティ **PR_RTF_COMPRESSEDプロパティの** 両方を設定します。 
  
メッセージ ストアが RTF 対応の場合は **、PR_RTF_COMPRESSEDプロパティのみを** 設定する必要があります。 
  
 **必要にPR_RTF_COMPRESSED同期プロセスが実行されるのを確認するには、RTF 対応のクライアント**
  
1. [IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出して **、PR_RTF_COMPRESSED** プロパティを開き、MAPI_CREATEフラグMAPI_MODIFYします。 MAPI_CREATE、新しいデータが古いデータに置き換わり、MAPI_MODIFY置き換えできます。 
    
2. メッセージ ストアが PR_STORE_SUPPORT_MASK プロパティに STORE_UNCOMPRESSED_RTF ビットを設定する場合は、WrapCompressedRTFStream 関数を呼び出し **、STORE_UNCOMPRESSED_RTF** を渡して **、OpenProperty** から返される PR_RTF_COMPRESSED ストリームの非圧縮バージョンを取得します。 [](wrapcompressedrtfstream.md) 
    
3. **WrapCompressedRTFStream** から返される非圧縮ストリームにメッセージ テキスト データを書き込みます。
    
4. 圧縮されていないストリームと圧縮されたストリームの両方をコミットして解放します。
    
この時点で、メッセージ ストア プロバイダーが RTF をサポートしている場合は、必要なすべての処理を行いました。 必要に応じて、メッセージ ストア プロバイダーに依存して、同期プロセスと PR_BODY プロパティ **の** 作成を処理できます。 ただし、メッセージ ストア プロバイダーが RTF をサポートしていない場合は [、RTFSync](rtfsync.md) 関数を呼び出してテキストを書式設定と同期し、RTF_SYNC_RTF_CHANGEDする必要があります。 
  

