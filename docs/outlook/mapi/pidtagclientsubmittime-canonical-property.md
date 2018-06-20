---
title: PidTagClientSubmitTime の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ccf4a6054ecc89e280f2f5cbc4c72b2a8a829055
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802541"
---
# <a name="pidtagclientsubmittime-canonical-property"></a>PidTagClientSubmitTime の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージの送信者にメッセージが送信されたときの日時が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_CLIENT_SUBMIT_TIME  <br/> |
|識別子:  <br/> |0x0039  <br/> |
|データを入力します。  <br/> |PT_SYSTIME  <br/> |
|領域:  <br/> |メッセージの時刻  <br/> |
   
## <a name="remarks"></a>備考

ストア プロバイダーは、クライアント アプリケーションが[IMessage::SubmitMessage](imessage-submitmessage.md)を呼び出したときに**PR_CLIENT_SUBMIT_TIME**を設定します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
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

