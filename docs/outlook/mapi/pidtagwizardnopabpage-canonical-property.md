---
title: PidTagWizardNoPabPage の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b393155d00b47fa8cce23c1b5ac7043237a58983
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803689"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a>PidTagWizardNoPabPage の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
このプロパティには、プロファイル ウィザードでは、個人用アドレス帳 (PAB) のページを非表示にする場合は TRUE が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_WIZARD_NO_PAB_PAGE  <br/> |
|識別子:  <br/> |0x6701  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |Exchange の管理  <br/> |
   
## <a name="remarks"></a>備考

サービス プロバイダーは、 [LAUNCHWIZARDENTRY](launchwizardentry.md)関数のプロトタイプでは関数を呼び出すときにこのプロパティを設定できます。 このプロパティは、プロバイダーがユーザー ダイアログ ボックスの中に表示される個人用アドレス帳ページをしないことをプロファイル ウィザードに指示します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

