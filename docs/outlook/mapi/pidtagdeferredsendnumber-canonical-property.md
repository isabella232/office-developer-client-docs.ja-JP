---
title: PidTagDeferredSendNumber の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendNumber
api_type:
- HeaderDef
ms.assetid: 8ada5c9b-bec5-42d8-bc58-f0411ec4e88b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f2ccd004415bcbd42b56b1269fbdb4622ef1f8c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802699"
---
# <a name="pidtagdeferredsendnumber-canonical-property"></a>PidTagDeferredSendNumber の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージの送信の繰延を計算するために使用できる番号が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_DEFERRED_SEND_NUMBER  <br/> |
|識別子:  <br/> |0x3FEB  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、ファイルが存在しない場合は、 **PR_DEFERRED_SEND_TIME** ([PidTagDeferredSendTime](pidtagdeferredsendtime-canonical-property.md)) のプロパティを計算するために使用します。 **PR_DEFERRED_SEND_TIME**プロパティが存在しない場合、メッセージの送信が遅延すると、 **PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) のプロパティと**PR_DEFERRED_SEND_NUMBER**プロパティを設定してください。 
  
**PR_DEFERRED_SEND_NUMBER**値は、0 から 999 の間で設定する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
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
