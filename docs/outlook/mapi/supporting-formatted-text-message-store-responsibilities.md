---
title: 書式設定されたテキスト メッセージ ストアの責任をサポートする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a97993c2-52e4-4b71-ac03-2c02d82447d8
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 502ba82279664638c8e7e4ae68f74df74758918d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435517"
---
# <a name="supporting-formatted-text-message-store-responsibilities"></a>書式設定されたテキストのサポート: メッセージ ストアの責任

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーは **、PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) プロパティを使用して、リッチ テキスト形式 (RTF)、HTML テキスト、および RTF 対応の場合は、書式設定されたテキストを圧縮形式または非圧縮形式で保存できるかどうかを発行します。 メッセージ ストア プロバイダーは、STORE_RTF_OK ビットを設定して RTF に対応し、STORE_UNCOMPRESSED_RTF ビットを設定して、書式設定されたテキストを圧縮されていない形式で格納STORE_UNCOMPRESSED_RTFします。 メッセージ ストア プロバイダーは、ビットを設定して HTML に対応STORE_HTML_OKします。
  
メッセージ ストアが RTF をサポートするかどうかを判断するには、RTF 対応クライアントが STORE_RTF_OK ビットを確認することが重要ですが、クライアントが RTF 対応ストアの書式設定されたテキストの形式を気にしている必要はありません。 
  
すべてのメッセージ ストアは、RTF 対応以外のクライアントをサポートする必要があります。 クライアントが PR_RTF_IN_SYNC または **PR_RTF_COMPRESSED** **(** [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) を更新せずに **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) を変更した場合、RTF 対応以外のメッセージ ストアは、メッセージの [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドの呼び出し中に PR_RTF_IN_SYNC ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) プロパティを削除する必要があります。 この **PR_RTF_IN_SYNC** するとPR_RTF_COMPRESSED RTF 対応のクライアントが次回 RTFSync を呼び出すPR_BODY プロパティから PR_BODY プロパティが [再計算されます](rtfsync.md)。 
  
ほとんどの RTF 対応のメッセージ ストアには、クライアントからメッセージ テキストが与えされません。要求に応じて計算する必要があります。 この計算は時間とコストがかかるため、クライアントは可能な限 **りPR_RTF_COMPRESSEDを** 使用する必要があります。 PR_BODY プロパティ **を計算するには** 、メッセージ ストア プロバイダーが PR_RTF_COMPRESSED プロパティ **の内容** を圧縮解除し、リッチ テキストの書式設定を削除する必要があります。 PR_RTF_COMPRESSED プロパティをサポートしていない **クライアントでは、** すべてのメッセージに対してこの計算を実行する必要があります。 
  
メッセージをコピーする場合 **、IMAPISupport::D oCopyProps または IMAPISupport::D oCopyTo** メソッドを使用しないメッセージ ストア プロバイダーは、実装が **PR_BODY** プロパティを除外し、PR_RTF_COMPRESSED に依存している場合、コンテンツを含むメッセージを作成する危険性があります。  プロパティ内のデータが **破損** PR_RTF_COMPRESSED可能性があります。 コピー操作でこれらのメッセージ コンテンツ プロパティのいずれかを除外する前に、次のように破損を確認してください。 
  
1. 圧縮された RTF **PR_RTF_COMPRESSED値** が大きい場合、プロパティは壊れています。 
    
2. RTF ヘッダーのマジック値が  _dwMagicCompressedRTF_ または  _dwMagicUncompressedRTF_ ではない場合、プロパティは壊れています。
    
サポート メソッドを使用するメッセージ ストア プロバイダーは、破損のチェックを実装 **PR_RTF_COMPRESSED** 必要があります。MAPI を使用すると、適切なプロパティが存在し、有効になります。 
  
メッセージ ストア プロバイダーが実装できる RTF サポートには、3 つの異なるレベルがあります。MAPI では、RTF 対応のメッセージ ストア プロバイダーが中央または最高レベルでサポートを実装する必要があります。 すべての RTF 対応メッセージ ストア プロバイダーは、送信メッセージの **PR_RTF_COMPRESSED** に含まれるデータから **PR_BODY** を生成し、受信メッセージのテキストと書式設定を同期するために **RTFSync** を呼び出します。 
  
これら 3 つのレベルの違いを次の表に示します。 
  
|**サポートのレベル**|**説明**|
|:-----|:-----|
|低い  <br/> |メッセージ ストア プロバイダーは、変更がメッセージに保存されるたびに **RTFSync** を呼び出し、PR_RTF_COMPRESSED から **PR_BODY** プロパティのデータを抽出します **。** データ **PR_BODY** と **PR_RTF_COMPRESSED** が格納されます。  <br/> |
|Middle  <br/> |メッセージ ストア プロバイダーは、必要に応 **じてPR_RTF_COMPRESSEDプロパティ** のみをPR_BODY **格納します** 。  <br/> |
|高い  <br/> |メッセージ ストア プロバイダーは、PR_BODY **RTF** プロパティも格納されません。 **RTFSync** は、メッセージ テキストが変更され、書式設定が変更されていない場合、またはトランスポート プロバイダーによって新しいメッセージがダウンロードされた場合に呼び出されます。  <br/> |
   

