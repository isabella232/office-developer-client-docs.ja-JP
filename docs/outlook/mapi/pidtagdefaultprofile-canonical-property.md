---
title: PidTagDefaultProfile の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultProfile
api_type:
- HeaderDef
ms.assetid: 47f745a4-5a9c-42af-b076-a72548ef4d31
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6cd255c60987ec7a279e509aa2925a8029cce62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802649"
---
# <a name="pidtagdefaultprofile-canonical-property"></a>PidTagDefaultProfile の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージング ユーザー プロファイルが既定の MAPI プロファイルの場合、TRUE が格納されます。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_DEFAULT_PROFILE  <br/> |
|識別子:  <br/> |0x3D04  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |MAPI プロファイル  <br/> |
   
## <a name="remarks"></a>備考

プロファイル テーブルに列としてのみですが、任意のオブジェクトのプロパティとしては、このプロパティは表示されません。 クライアント アプリケーションは、既定のプロファイルを指定するのには[IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md)メソッドを使用することができます。 
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagDefaultStore の標準的なプロパティ](pidtagdefaultstore-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

