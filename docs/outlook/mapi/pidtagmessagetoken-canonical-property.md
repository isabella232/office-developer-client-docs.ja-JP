---
title: PidTagMessageToken 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToken
api_type:
- HeaderDef
ms.assetid: fcb93346-db92-44b5-a447-59fd95f98f45
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2d832b3a53f8056c034b5e87f1f309fa3058173d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408188"
---
# <a name="pidtagmessagetoken-canonical-property"></a>PidTagMessageToken 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの ASN.1 セキュリティ トークンが含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_TOKEN  <br/> |
|識別子:  <br/> |0x0C03  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |セキュリティで保護されたメッセージングのプロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、保護されたセキュリティ関連の情報を発信元から受信者に伝達します。 PR_MESSAGE_SECURITY_LABEL **(** [PidTagMessageSecurityLabel](pidtagmessagesecuritylabel-canonical-property.md)) プロパティと組み合わせて、ラベルとメッセージ コンテンツとの関連付けを保証します。 このプロパティは **、PR_CONTENT_INTEGRITY_CHECK** ([PidTagContentIntegrityCheck)](pidtagcontentintegritycheck-canonical-property.md)プロパティと組み合わせて、メッセージの内容が変更されていないか確認します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 関連付けられたプロパティとして一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

