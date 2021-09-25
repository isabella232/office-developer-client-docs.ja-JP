---
title: PidTagControlFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fdfa27d06dcfb3542c03575b51b6483410266985
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613619"
---
# <a name="pidtagcontrolflags-canonical-property"></a>PidTagControlFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから作成されたダイアログ ボックスで使用されるコントロールの動作を制御するフラグのビットマスクが含まれる。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTROL_FLAGS  <br/> |
|識別子:  <br/> |0x3F00  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 表示テーブル  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには、次のフラグを 1 つ以上設定できます。
  
DT_ACCEPT_DBCS 
  
> コントロールには、Double-Byte文字セット (DBCS) 文字を含めることができます。 このフラグは、編集コントロールと一緒に使用されます。 複数バイトの文字セットを使用できます。
    
DT_EDITABLE 
  
> コントロールは編集できます。コントロールに関連付けられている値を変更できます。 このフラグが設定されていない場合、コントロールは読み取り専用です。 ラベル、グループ ボックス、標準プッシュ ボタン、複数値のドロップダウン リスト ボックス、およびリスト ボックス コントロールでは、この値は無視されます。
    
DT_MULTILINE 
  
> 編集コントロールには複数の行を含めできます。 つまり、コントロール内に戻り文字を入力できます。 このフラグは、編集コントロールでのみ有効です。
    
DT_PASSWORD_EDIT 
  
> 編集コントロールに適用されます。 編集コントロールはパスワードのように扱います。 値は、入力された実際の文字をエコーするのではなく、アスタリスクを使用して表示されます。
    
DT_REQUIRED 
  
> コントロールで変更を許可する場合 [(DT_EDITABLE)、IMAPIProp::SaveChanges](imapiprop-savechanges.md) が呼び出される前に値が必要です。 
    
DT_SET_IMMEDIATE 
  
> 値の即時設定を有効にします。コントロールの値が変更されたとすぐに、MAPI は、そのコントロールに関連付けられているプロパティの **SetProps** メソッドを呼び出します。 このフラグを設定しない場合、ダイアログ ボックスが閉じらされた時点で値が設定されます。 
    
DT_SET_SELECTION 
  
> リスト ボックス内で選択が行われた場合、そのリスト ボックスのインデックス列はプロパティとして設定されます。 常に、DT_SET_IMMEDIATE。
    
このプロパティは、コントロールの DTCTL 構造の ulCtlFlags [メンバーに格納](dtctl.md) されます。 ほとんどのコントロール フラグは、ユーザー入力を許可するすべてのコントロールに適用されます。編集コントロールにのみ適用される場合があります。 ボタンやラベルなどのユーザー入力を許可しないコントロールは、コントロール フラグに 0 を設定します。 
  
フラグ値の多くは、自明です。 たとえば、コントロールDT_REQUIRED設定されている場合は、ダイアログ ボックスを閉じ込む前に値を含む必要があります。 サービス プロバイダーが **IMAPIProp** 実装を通じて値を指定するか、ユーザーが値を入力できます。 DT_EDITABLEコントロールの値を変更できます。 DT_MULTILINE編集コントロールの値を複数行にまたがって指定できます。 
  
一部のコントロール フラグは、その意味では明らかではありません。 コントロールが DT_SET_IMMEDIATEフラグを設定すると、その値に対する変更は、ユーザーが新しいコントロールに移動するとすぐに影響を受ける。 MAPI は、コントロールのプロパティのプロパティ インターフェイス [の IMAPIProp::SetProps](imapiprop-setprops.md) メソッドを 1 回呼び出します。 これは既定の動作とは異なります。これは、ユーザーが **[OK]** ボタンを選択するか、ダイアログ ボックスを閉じるまで、コントロールの値に変更を加えるのを延期する方法です。 このDT_SET_IMMEDIATEは、多くの場合、表示テーブル通知と組み合わせて使用されます。 
  
次の表に、コントロールの種類と、各種類に設定できるすべてのフラグ値を示します。
  
|**Control**|**このプロパティの有効な値**|
|:-----|:-----|
|ボタン  <br/> |0 である必要があります  <br/> |
|チェック ボックス  <br/> |DT_EDITABLE、DT_SET_IMMEDIATE  <br/> |
|コンボ ボックス  <br/> |DT_EDITABLE、DT_REQUIRED、DT_SET_IMMEDIATE  <br/> |
|ドロップダウン リスト ボックス  <br/> |DT_EDITABLE、DT_SET_IMMEDIATE  <br/> |
|編集  <br/> |DT_ACCEPT_DBCS、DT_MULTILINE、DT_EDITABLE、DT_PASSWORD_EDIT、DT_REQUIRED、DT_SET_IMMEDIATE  <br/> |
|グループ ボックス  <br/> |0 である必要があります  <br/> |
|ラベル  <br/> |0 である必要があります  <br/> |
|リスト ボックス  <br/> |0 である必要があります  <br/> |
|[複数値] ドロップダウン リスト ボックス  <br/> |0 である必要があります  <br/> |
|複数値リスト ボックス  <br/> |0 である必要があります  <br/> |
|タブ付きページ  <br/> |0 である必要があります  <br/> |
|ラジオ ボタン  <br/> |0 である必要があります  <br/> |
   
## <a name="related-resources"></a>関連リソース

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

