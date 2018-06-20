---
title: PidTagProviderParentItemId の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderParentItemId
api_type:
- COM
ms.assetid: 6adb8e85-ae56-4542-8b19-ed3cfe7fe522
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 96a9d153fadbe8b4c8baa8532b8c99771b1d7987
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803210"
---
# <a name="pidtagproviderparentitemid-canonical-property"></a>PidTagProviderParentItemId の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
フォルダーまたはストア内のアイテムの親の識別子を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_PROVIDER_PARENT_ITEMID  <br/> |
|識別子:  <br/> |0x0EA4  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>備考

ストア プロバイダーは、フォルダーまたはアイテムの親に対してこのプロパティの値を指定できますが、セッション間で同じように値が保持する必要があります。 ストア プロバイダーは、検索エンジンから返される検索結果を識別するのには、このプロパティを使用します。
  
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

