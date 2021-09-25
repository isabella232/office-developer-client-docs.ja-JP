---
title: PidTagProfileName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 65c2f1491be5205b3dadeb6c32d59e77be9bfda2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591691"
---
# <a name="pidtagprofilename-canonical-property"></a>PidTagProfileName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルの名前を含む。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_PROFILE_NAME、PR_PROFILE_NAME_A、PR_PROFILE_NAME_W  <br/> |
|識別子:  <br/> |0x3D12  <br/> |
|データの種類 :   <br/> |PT_STRING8、PT_UNICODE  <br/> |
|エリア:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>注釈

これらのプロパティは、サービス プロバイダーによって計算されます。 プロバイダーの **ServiceEntry** 関数の実装では、これらのプロパティを使用してプロファイル名を検出できます。 
  
クライアント アプリケーションは、MAPI サブシステムの状態テーブル行で **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを調べることで、プロファイル名を取得する便利な代替手段としてこれらのプロパティを使用できます。
  
これらのプロパティは、プロファイルが削除され、後で同じ名前で再作成されるなど、時間の間に一意ではない場合があります。 MAPI は、PR_SEARCH_KEY **と呼** ばれるハードコードされたプロファイル セクションに、完全に一意のプロパティ ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティ **MUID_PROFILE_INSTANCE。**
  
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

