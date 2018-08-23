---
title: PidTagTnefUnprocessedProps 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefUnprocessedProps
api_type:
- COM
ms.assetid: df9cd614-1198-44a2-9bf5-36c57179a9a9
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c25888353857f9233ba487661f5f27d64cd678cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577430"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a>PidTagTnefUnprocessedProps 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
トランスポート ニュートラル カプセル化形式 (TNEF) をフィルター処理する場合は、プロパティをシリアル化します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_TNEF_UNPROCESSED_PROPS  <br/> |
|識別子:  <br/> |0x0E9C  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>注釈

TNEF が名前付きのプロパティ ストア内に作成することはできませんが含まれている場合に元の TNEF を保存するために、Microsoft Outlook と Outlook Web Access (OWA) によって使用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

