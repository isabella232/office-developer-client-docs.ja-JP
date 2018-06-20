---
title: PidTagSupplementaryInfo の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIi.PidTagSupplementaryInfo
api_type:
- COM
ms.assetid: 2d4231b5-4096-4c0d-b694-65e2d04172b8
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 6f9d383b6be2ce8efc135b85e9bea151df535cfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803628"
---
# <a name="pidtagsupplementaryinfo-canonical-property"></a>PidTagSupplementaryInfo の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
レポートで使用するための追加情報が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_SUPPLEMENTARY_INFO、PR_SUPPLEMENTARY_INFO_A、PR_SUPPLEMENTARY_INFO_W  <br/> |
|識別子:  <br/> |0x0C1B  <br/> |
|データを入力します。  <br/> |PT_STRING8、PT_UNICODE  <br/> |
|領域:  <br/> |MAPI 受信者  <br/> |
   
## <a name="remarks"></a>備考

これらのプロパティには、メッセージ転送エージェントによって生成される情報が含まれているか、トランスポート プロバイダーは、レポートに関連します。 配信または配信不能レポートのテキストの基になるメッセージング システムに送信された場合に通常使用されます。
  
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

