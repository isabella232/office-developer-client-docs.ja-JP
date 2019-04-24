---
title: PidTagProfileName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 992b3a6a30e15d267ffeda11ec98c7b4aeacb2c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341651"
---
# <a name="pidtagprofilename-canonical-property"></a>PidTagProfileName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルの名前が含まれます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROFILE_NAME、PR_PROFILE_NAME_A、PR_PROFILE_NAME_W  <br/> |
|識別子:  <br/> |0x3d12  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>解説

これらのプロパティは、サービスプロバイダーによって計算されます。 プロバイダーの**serviceentry**関数の実装では、これらのプロパティを使用してプロファイル名を検出できます。 
  
クライアントアプリケーションは、これらのプロパティを使用して、プロファイル名を取得する便利な方法として、MAPI サブシステムの状態テーブル行の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを調べることができます。
  
これらのプロパティは、プロファイルが削除された後に同じ名前で再作成された場合など、時間の経過とともに一意になることはありません。 MAPI furnishes は、MUID_PROFILE_INSTANCE という名前のハードコーディングされたプロファイルセクションで、完全に一意の**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティを**示しています。**
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

