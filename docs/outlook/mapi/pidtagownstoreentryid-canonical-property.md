---
title: PidTagOwnStoreEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOwnStoreEntryId
api_type:
- COM
ms.assetid: 6a82ee90-10a1-49e0-8f3a-a2cd9f490f99
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 16a23c4e711bf9f7b670dff8b3e8f65371aa6bda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427375"
---
# <a name="pidtagownstoreentryid-canonical-property"></a>PidTagOwnStoreEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポートの密結合メッセージストアのエントリ id を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_OWN_STORE_ENTRYID  <br/> |
|識別子:  <br/> |0x3e06  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージストアのプロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、密結合ストアがある場合は、そのエントリ識別子を指定します。 たとえば、トランスポートプロバイダーは、パブリックフォルダーストアエントリ識別子を指定して、MAPI スプーラーがトランスポートプロバイダーをストアに接続できるようにすることができます。
  
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

