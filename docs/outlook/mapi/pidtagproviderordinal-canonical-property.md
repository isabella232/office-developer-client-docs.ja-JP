---
title: PidTagProviderOrdinal の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderOrdinal
api_type:
- COM
ms.assetid: d062b54d-7c32-4369-ab69-f7193773a1c0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b56ee557884e12728c98827f9eb1a280d7a29c30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803220"
---
# <a name="pidtagproviderordinal-canonical-property"></a>PidTagProviderOrdinal の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
プロバイダー テーブル内のサービス プロバイダーの位置の 0 から始まるインデックスが含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_PROVIDER_ORDINAL  <br/> |
|識別子:  <br/> |0x300D  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |一般的な MAPI  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、MAPI によって計算されます。
  
プロバイダー テーブルを取得するには、 [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md)メソッドを呼び出します。 トランスポートの順番を表示するには、このプロパティのプロバイダー テーブルを並べ替えます。 
  
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
