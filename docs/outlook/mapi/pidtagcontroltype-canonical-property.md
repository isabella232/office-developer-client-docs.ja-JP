---
title: PidTagControlType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlType
api_type:
- HeaderDef
ms.assetid: 7728fa2f-4a59-4e86-90f1-4384824598aa
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8614441ffa60181366c860b66ef4618ce32106be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334735"
---
# <a name="pidtagcontroltype-canonical-property"></a>PidTagControlType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ダイアログボックスで使用されるコントロールのコントロールの種類を示す値を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTROL_TYPE  <br/> |
|識別子:  <br/> |0x3f02  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 表示テーブル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、次のいずれかの値を指定できます。
  
DTCT_BUTTON 
  
> ダイアログボタンコントロール。
    
DTCT_CHECKBOX 
  
> ダイアログのチェックボックス。
    
DTCT_COMBOBOX 
  
> ダイアログボックスのコンボボックス。
    
DTCT_DDLBX 
  
> ダイアログボックスのドロップダウンリストボックス。
    
DTCT_EDIT 
  
> ダイアログボックスの編集テキストボックス。
    
DTCT_GROUPBOX 
  
> ダイアロググループボックス。
    
DTCT_LABEL 
  
> ダイアログのラベル。
    
DTCT_LBX 
  
> ダイアログボックスのリストボックス。
    
DTCT_LISTBOX 
  
> ダイアログボックスのリストボックス。
    
DTCT_MVDDLBX 
  
> 文字列型の複数値プロパティによって設定された複数値のリストボックス。
    
DTCT_PAGE 
  
> ダイアログのタブ付きページ。
    
DTCT_RADIOBUTTON 
  
> ダイアログのラジオボタン。
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

