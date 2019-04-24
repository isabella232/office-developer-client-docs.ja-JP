---
title: PidTagOriginatingMtaCertificate 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatingMtaCertificate
api_type:
- COM
ms.assetid: f6b7ff0c-19a0-4cad-8868-c05397fcebf4
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6f78609537b85a89617e7b2fa8f30a4ba952805b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340937"
---
# <a name="pidtagoriginatingmtacertificate-canonical-property"></a>PidTagOriginatingMtaCertificate 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを発信したメッセージ転送エージェント (MTA) の識別子が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_ORIGINATING_MTA_CERTIFICATE  <br/> |
|識別子:  <br/> |0x0e25  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |サーバー  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、[送信済みアイテム] フォルダーの送信されたメッセージに対して設定されている場合に使用できます。
  
このプロパティは、メッセージごとの400レポート属性に対応します。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 関連するプロパティとしてリストされているプロパティの定義が含まれます。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

