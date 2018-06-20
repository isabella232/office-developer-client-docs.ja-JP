---
title: PidTagProfileName の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6ecd84e4ffa0959a037574998b5ff12d8f539c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803197"
---
# <a name="pidtagprofilename-canonical-property"></a>PidTagProfileName の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
プロファイルの名前が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_PROFILE_NAME、PR_PROFILE_NAME_A、PR_PROFILE_NAME_W  <br/> |
|識別子:  <br/> |0x3D12  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI プロファイルの構成  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティは、サービス プロバイダーによって計算されます。 **ServiceEntry**関数のプロバイダーの実装では、プロファイル名を検出するのにはこれらのプロパティを使用できます。 
  
クライアント アプリケーションでは、MAPI サブシステムの状態テーブルの行の**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを調べることによって、プロファイル名を取得するための便利な方法として、これらのプロパティを使用できます。
  
これらのプロパティが一意でくださいない時、たとえば、プロファイルが削除され、同じ名前の後で再作成で。 MAPI と呼ばれるハード コーディングされたプロファイル セクションで完全に一意の**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) プロパティを提供する**MUID_PROFILE_INSTANCE です**。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

