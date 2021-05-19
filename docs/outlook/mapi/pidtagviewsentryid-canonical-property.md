---
title: PidTagViewsEntryId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewsEntryId
api_type:
- COM
ms.assetid: 8350a37c-6f42-4bef-82e0-35aa12b09fcf
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7d261ac0e9aaf36f2333b04b45edfaf8e24fa30d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427312"
---
# <a name="pidtagviewsentryid-canonical-property"></a>PidTagViewsEntryId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ユーザー定義の Views フォルダーのエントリ識別子を格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_VIEWS_ENTRYID  <br/> |
|識別子:  <br/> |0x35E5  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>注釈

共通ビュー フォルダーには定義済みの標準ビュー指定子のセットが含まれる一方、ビュー フォルダーにはメッセージング ユーザーによって定義された指定子が含まれる。 これらのフォルダーは、対人間メッセージ (IPM) 階層には表示されませんが、多くのビュー指定子を保持できます。各フォルダーはメッセージとして保存されます。 クライアント アプリケーションでは、2 つの指定子セットを結合し、両方を使用できます。
  
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

