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
ms.openlocfilehash: 3c1d415cc9aa4e66b6c4b17262f9a491fc01f6bd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574126"
---
# <a name="pidtagcontroltype-canonical-property"></a>PidTagControlType 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ダイアログ ボックスで使用されているコントロールのコントロールの種類を示す値が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTROL_TYPE  <br/> |
|識別子:  <br/> |0x3F02  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI 表示テーブル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、次の値の 1 つだけ持つことができます。
  
DTCT_BUTTON 
  
> ダイアログ ボタン コントロールです。
    
DTCT_CHECKBOX 
  
> ダイアログのチェック ボックスです。
    
DTCT_COMBOBOX 
  
> ダイアログのコンボ ボックス。
    
DTCT_DDLBX 
  
> ダイアログ ボックスの一覧ボックスです。
    
DTCT_EDIT 
  
> ダイアログ編集テキスト ボックスです。
    
DTCT_GROUPBOX 
  
> グループ] ダイアログ ボックスです。
    
DTCT_LABEL 
  
> ダイアログのラベルです。
    
DTCT_LBX 
  
> ダイアログ ボックスの一覧ボックスです。
    
DTCT_LISTBOX 
  
> ダイアログ ボックスの一覧ボックスです。
    
DTCT_MVDDLBX 
  
> 文字列型の複数値を持つプロパティによって設定されます。 複数値を持つリスト ボックスです。
    
DTCT_PAGE 
  
> ダイアログのタブ付きページです。
    
DTCT_RADIOBUTTON 
  
> ダイアログ オプション ボタン。
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

