---
title: PidLidRemoteTransport 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 124a0d8f23fcff9d1bca9d5debe4a9aa6fb6146c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587118"
---
# <a name="pidlidremotetransport-canonical-property"></a>PidLidRemoteTransport 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
どのようなアカウントのヘッダー項目に関連付けられて、POP を置くサーバーの機能に実装するには、主に識別します。 
  
|||
|:-----|:-----|
|関連するプロパティ  <br/> |dispidRemoteXP  <br/> |
|プロパティを設定します。  <br/> |PSETID_Remote  <br/> |
|長い ID (LID):  <br/> |0x00008F03  <br/> |
|データの種類 :   <br/> |PT_STRING8  <br/> |
|領域:  <br/> |リモート ・ メッセージ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、メッセージ クラスは IPM メッセージだけに関連します。リモートです。 Microsoft Outlook フォルダー関連の情報 (FAI) メッセージでは、特定の店舗へのダウンロードは、さまざまなアカウントのマッピングを保持するが、この情報をレジストリにも保存できます。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[MS OXPROPS] 
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

