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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7bdb02f72ba14a36c8a4c218cd5f0631e7145e6a
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734204"
---
# <a name="pidtagcontroltype-canonical-property"></a>PidTagControlType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ダイアログ ボックスで使用されるコントロールのコントロールの種類を示す値を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTROL_TYPE  <br/> |
|識別子:  <br/> |0x3F02  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 表示テーブル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、次のいずれかの値を指定できます。
    
DTCT_LABEL (0x00000000)
  
> ダイアログ ラベル。
   
DTCT_EDIT (0x000000001)
  
> ダイアログの編集テキスト ボックス。

DTCT_LBX (0x000000002)
  
> ダイアログ リスト ボックス。
    
DTCT_COMBOBOX (0x00000003)
  
> ダイアログ コンボ ボックス。

DTCT_DDLBX (0x000000004)
  
> ダイアログ ボックスのドロップダウン リスト ボックス。

DTCT_CHECKBOX (0x00000005)
  
> ダイアログ チェック ボックス。

DTCT_GROUPBOX (0x00000006)
  
> ダイアログ グループ ボックス。
  
DTCT_BUTTON (0x00000007)
  
> ダイアログ ボタン コントロール。
    
DTCT_PAGE (0x000000008)
  
> タブ付きダイアログ ページ。
    
DTCT_RADIOBUTTON (0x00000009)
  
> ダイアログのラジオ ボタン。
    
DTCT_MVLISTBOX (0x0000000B)
  
> 文字列型の複数値プロパティによって設定される複数値リスト ボックス。
    
DTCT_MVDDLBX (0x0000000C)
  
> 文字列型の複数値プロパティによって設定される複数値ドロップダウン リスト ボックス。
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
mapitags.h
  
> 代替名として表示されるプロパティの定義を含む。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名と MAPI 名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名と標準プロパティ名のマッピング](mapping-mapi-names-to-canonical-property-names.md)

