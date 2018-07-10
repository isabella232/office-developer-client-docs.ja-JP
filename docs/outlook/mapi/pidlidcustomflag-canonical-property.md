---
title: PidLidCustomFlag の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5d97f56946512266bb7a08aa6b4a4ff78dded56a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801868"
---
# <a name="pidlidcustomflag-canonical-property"></a>PidLidCustomFlag の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
指定するビットマスク メッセージは、カスタマイズ方法、たとえば、カスタム プロパティを保存します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidCustomFlag  <br/> |
|長い ID (LID):  <br/> |0x00008251  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>備考

このプロパティの値を取得するには、まず**[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** を使用して、プロパティ タグを取得して値を取得する**[IMAPIProp::GetProps](imapiprop-getprops.md)** でこのプロパティのタグを指定します。 
  
使用できるフラグは次のとおりです。
  
****

|**定数**|**値**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
**IMAPIProp::GetIDsFromNames**を呼び出すときは、 *lppPropNames*の入力パラメーターで指定された**[MAPINAMEID](mapinameid.md)** 構造体の次の値を指定します。 
  
****

|**メンバー**|**値**|
|:-----|:-----|
|lpGuid。  <br/> |PSETID_Common  <br/> |
|ulKind。  <br/> |MNID_ID  <br/> |
|Kind.lID。  <br/> |dispidCustomFlag  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義を提供します。
    
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
