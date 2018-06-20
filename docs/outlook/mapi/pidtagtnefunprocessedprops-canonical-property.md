---
title: PidTagTnefUnprocessedProps の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ee05f2e539d379e8fe197161fa0f6453add31afb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803638"
---
# <a name="pidtagtnefunprocessedprops-canonical-property"></a>PidTagTnefUnprocessedProps の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
トランスポート ニュートラル カプセル化形式 (TNEF) をフィルター処理する場合は、プロパティをシリアル化します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_TNEF_UNPROCESSED_PROPS  <br/> |
|識別子:  <br/> |0x0E9C  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI 以外から送信できます。  <br/> |
   
## <a name="remarks"></a>備考

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
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

