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
  
トランスポートの緊密に結合されたメッセージ ストアのエントリ識別子を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_OWN_STORE_ENTRYID  <br/> |
|識別子:  <br/> |0x3E06  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |メッセージ ストアのプロパティ  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、緊密に結合されたストアのエントリ識別子 (存在する場合) を指定します。 たとえば、MAPI スプーラーがトランスポート プロバイダーをストアに接続できるよう、トランスポート プロバイダーはプライベート フォルダー ストアエントリ識別子を指定できます。
  
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

