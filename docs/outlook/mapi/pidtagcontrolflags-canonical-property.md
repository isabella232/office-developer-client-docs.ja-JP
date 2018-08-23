---
title: PidTagControlFlags 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlFlags
api_type:
- HeaderDef
ms.assetid: b97a9e72-fbb7-49ab-a19d-5e9bd1b8a80d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fc47dc88ed0618bcdf46c309776d5a871d2128e9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580741"
---
# <a name="pidtagcontrolflags-canonical-property"></a>PidTagControlFlags 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
ディスプレイ テーブルから作成されたダイアログ ボックスで使用するコントロールの動作を制御するフラグのビットマスクを格納します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTROL_FLAGS  <br/> |
|識別子:  <br/> |0x3F00  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI 表示テーブル  <br/> |
   
## <a name="remarks"></a>注釈

次のフラグの 1 つ以上は、このプロパティを設定できます。
  
DT_ACCEPT_DBCS 
  
> コントロールは、これで 2 バイト文字セット (DBCS) 文字を持つことができます。 このフラグは、エディット コントロールで使用されます。 複数バイト文字セットは、できます。
    
DT_EDITABLE 
  
> コントロールを編集することができます。コントロールに関連付けられている値を変更することができます。 このフラグが設定されていない場合、コントロールが読み取り専用にします。 複数値ドロップダウン リスト ボックスとリスト ボックス コントロール、ラベル、グループ ボックス、標準のプッシュ ボタンには、この値は無視されます。
    
DT_MULTILINE 
  
> エディット コントロールは、複数の行を含めることができます。 これは、コントロール内で戻り値の文字を入力できることを意味します。 このフラグは、エディット コントロールでのみ有効です。
    
DT_PASSWORD_EDIT 
  
> エディット コントロールに適用されます。 エディット コントロールは、パスワードのように扱われます。 実際に入力した文字をエコーするのではなくアスタリスクを使用して値が表示されます。
    
DT_REQUIRED 
  
> コントロールは、(DT_EDITABLE) の変更を許可している場合[IMAPIProp::SaveChanges](imapiprop-savechanges.md)が呼び出される前に値が必要です。 
    
DT_SET_IMMEDIATE 
  
> により即時の設定値のコントロールの値を変更するとすぐに、MAPI は、そのコントロールに関連付けられているプロパティの**SetProps**メソッドを呼び出します。 このフラグが設定されていない場合、ダイアログ ボックスを閉じるときに値が設定されます。 
    
DT_SET_SELECTION 
  
> リスト ボックス内で選択が行われると、そのリスト ボックスのインデックス列がプロパティとして設定されています。 常に DT_SET_IMMEDIATE を使用します。
    
このプロパティは、コントロールの[DTCTL](dtctl.md)構造体の ulCtlFlags メンバーに格納されます。 コントロール フラグのほとんどすべてのユーザーの入力を許可するコントロールに適用します。いくつかは、エディット コントロールにのみ適用されます。 ボタンやラベルなどのユーザー入力を許可しないコントロールは、コントロール フラグを 0 に設定します。 
  
フラグの値の多くは、説明されています。 たとえば、DT_REQUIRED 設定すると、コントロールのダイアログ ボックスが閉じられるまで許可される前に値でなければなりません。 サービス プロバイダーは、 **IMAPIProp**実装を通じて値を指定できますか、ユーザーがいずれかを入力します。 DT_EDITABLE は、コントロールの値を変更できることを示します。 DT_MULTILINE は、複数行にまたがって記述するエディット コントロールの値を使用できます。 
  
制御フラグがいくつかは、その意味で原因は定かではありません。 コントロールは、DT_SET_IMMEDIATE フラグを設定、ときにユーザーが新しいコントロールに移動するとすぐにその値を変更が影響します。 MAPI は、コントロールのプロパティの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドをプロパティのインターフェイスの 1 つの呼び出しです。 これは、ユーザーが **[ok]** ボタンを選択するか、ダイアログ ボックスを閉じるまで有効にするコントロールの値に変更することを延期するのには、既定の動作と異なります。 DT_SET_IMMEDIATE フラグ表示のテーブルの通知と組み合わせて使用されます。 
  
次の表は、コントロールの種類とそのすべての種類ごとに設定できるフラグの値の一覧です。
  
|**Control**|**このプロパティの有効な値**|
|:-----|:-----|
|ボタン  <br/> |0 にする必要があります。  <br/> |
|チェック ボックス  <br/> |DT_EDITABLE、DT_SET_IMMEDIATE  <br/> |
|コンボ ボックス  <br/> |DT_EDITABLE、DT_REQUIRED、DT_SET_IMMEDIATE  <br/> |
|ドロップダウン リスト ボックス  <br/> |DT_EDITABLE、DT_SET_IMMEDIATE  <br/> |
|編集  <br/> |DT_ACCEPT_DBCS、DT_MULTILINE、DT_EDITABLE、DT_PASSWORD_EDIT、DT_REQUIRED、DT_SET_IMMEDIATE  <br/> |
|グループ ボックス  <br/> |0 にする必要があります。  <br/> |
|ラベル  <br/> |0 にする必要があります。  <br/> |
|リスト ボックス  <br/> |0 にする必要があります。  <br/> |
|複数値ドロップダウン リスト ボックス  <br/> |0 にする必要があります。  <br/> |
|複数値リスト ボックス  <br/> |0 にする必要があります。  <br/> |
|タブ付きページ  <br/> |0 にする必要があります。  <br/> |
|ラジオ ボタン  <br/> |0 にする必要があります。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

