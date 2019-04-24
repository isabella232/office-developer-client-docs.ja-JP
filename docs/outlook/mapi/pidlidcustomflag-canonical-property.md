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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357618"
---
# <a name="pidlidcustomflag-canonical-property"></a>PidLidCustomFlag 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージをカスタマイズする方法を指定するビットマスク。たとえば、カスタムプロパティと共に保存されます。
  
## 

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidcustomflag  <br/> |
|ロング ID (LID):  <br/> |0x00008251  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>解説

このプロパティの値を取得するには、最初に**[imapiprop:: getidsfromnames](imapiprop-getidsfromnames.md)** を使用してプロパティタグを取得し、次に**[imapiprop:: GetProps](imapiprop-getprops.md)** でこのプロパティタグを指定して、値を取得します。 
  
可能なフラグは次のとおりです。
  
****

|**定数**|**値**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0d000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
**imapiprop:: getidsfromnames**を呼び出す場合は、入力パラメーター *lpppropnames*で示される**[mapinameid](mapinameid.md)** 構造体に次の値を指定します。 
  
****

|**Member**|**値**|
|:-----|:-----|
|lpguid:  <br/> |PSETID_Common  <br/> |
|ulkind:  <br/> |MNID_ID  <br/> |
|ふたの種類:  <br/> |dispidcustomflag  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義を提供します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

