---
title: PidTagOriginatorDeliveryReportRequested の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 07cea7606654bf32c1fe70e49254afeeb04f0e98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803126"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a>PidTagOriginatorDeliveryReportRequested の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージの送信者は、メッセージがメッセージ ・ ストアに配置される前に特定の受信者のメッセージング システムから、配信レポートを要求した場合、TRUE が格納されます。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED  <br/> |
|識別子:  <br/> |0x0023  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>備考

メッセージング システムに配信されるメッセージの処理を指示するこのプロパティを使用します。 この例では、メッセージは**PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) プロパティを FALSE に設定をも提供する必要があります。
  
**PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED**プロパティをメッセージの設定は、すべての受信者に対する配信状態レポートを要求する方法です。 
  
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

