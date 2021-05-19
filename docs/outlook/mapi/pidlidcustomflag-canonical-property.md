---
title: PidLidCustomFlag 標準プロパティ
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357618"
---
# <a name="pidlidcustomflag-canonical-property"></a>PidLidCustomFlag 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージをカスタマイズする方法を指定するビットマスク 。たとえば、カスタム プロパティを使用して保存します。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidCustomFlag  <br/> |
|長い ID (LID):  <br/> |0x00008251  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティの値を取得するには、まず **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** を使用してプロパティ タグを取得し **[、IMAPIProp::GetProps](imapiprop-getprops.md)** でこのプロパティ タグを指定して値を取得します。 
  
可能なフラグは次のとおりです。
  
****

|**定数**|**値**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
**IMAPIProp::GetIDsFromNames** を呼び出す場合は、入力パラメーター *lppPropNames* によって指される **[MAPINAMEID](mapinameid.md)** 構造体に次の値を指定します。 
  
****

|**メンバー**|**値**|
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidCustomFlag  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義を提供します。
    
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

