---
title: PidTagDeferredSendTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3912c429f1aa932b4956d943579a4ed99634dca2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802657"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a>PidTagDeferredSendTime の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
クライアントにはメッセージの送信を延期する時間を示します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_DEFERRED_SEND_TIME  <br/> |
|識別子:  <br/> |0x3FEF  <br/> |
|データを入力します。  <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>備考

次の数式を使用して、このプロパティの値が再計算、 **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) と**PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) のプロパティが存在する場合、以前の値は無視されます。
  
 **PR_DEFERRED_SEND_TIME** = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) + **PR_DEFERRED_SEND_NUMBER** * 水曜 (**PR_DEFERRED_SEND_UNITS**)
  
**PR_DEFERRED_SEND_TIME**の値が、現在の時刻 (UTC) より前の場合は、メッセージが直ちに送信されます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

