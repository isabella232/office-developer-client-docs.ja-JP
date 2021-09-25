---
title: PidTagTnefUnprocessedProps 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagTnefUnprocessedProps
api_type:
- COM
ms.assetid: df9cd614-1198-44a2-9bf5-36c57179a9a9
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a544e108be195edaf3bce3ebd6be6440db2b5d6a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609699"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a>PidTagTnefUnprocessedProps 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
トランスポート ニュートラル カプセル化形式 (TNEF) をフィルター処理するときにプロパティをシリアル化します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_TNEF_UNPROCESSED_PROPS  <br/> |
|識別子:  <br/> |0x0E9C  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI 送信不可  <br/> |
   
## <a name="remarks"></a>注釈

ストアで作成できない名前付きプロパティが TNEF に含まれている場合に、元の TNEF を保存するために Microsoft Outlook および Outlook Web Access (OWA) によって使用されます。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

