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
ms.openlocfilehash: 099f08876eadc83ebb66b9e4226eeeee6277bf01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331865"
---
# <a name="pidtagcontrolflags-canonical-property"></a>PidTagControlFlags 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示テーブルから構築されたダイアログボックスで使用されるコントロールの動作を制御するフラグのビットマスクを含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_CONTROL_FLAGS  <br/> |
|識別子:  <br/> |0x3f00  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI 表示テーブル  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、次の1つ以上のフラグを設定できます。
  
DT_ACCEPT_DBCS 
  
> コントロールは、2バイト文字セット (DBCS) 文字を持つことができます。 このフラグは、編集コントロールで使用されます。 複数バイト文字セットを使用できます。
    
DT_EDITABLE 
  
> コントロールを編集できます。コントロールに関連付けられている値を変更できます。 このフラグが設定されていない場合、コントロールは値の取得のみ可能です。 この値は、ラベル、グループボックス、標準プッシュボタン、複数値ドロップダウンリストボックス、およびリストボックスコントロールでは無視されます。
    
DT_MULTILINE 
  
> 編集コントロールには複数の行を含めることができます。 これは、コントロール内に戻り文字を入力できることを意味します。 このフラグは、編集コントロールに対してのみ有効です。
    
DT_PASSWORD_EDIT 
  
> 編集コントロールに適用されます。 編集コントロールは、パスワードと同じように扱われます。 値は、入力した実際の文字をエコーするのではなく、アスタリスクを使用して表示されます。
    
DT_REQUIRED 
  
> コントロールで変更が許可されている (DT_EDITABLE) 場合は、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)が呼び出される前に値を指定する必要があります。 
    
DT_SET_IMMEDIATE 
  
> 値の即時設定を有効にします。コントロールの値が変更されるとすぐに、MAPI は、そのコントロールに関連付けられているプロパティの**setprops**メソッドを呼び出します。 このフラグが設定されていない場合は、ダイアログボックスを閉じるときに値が設定されます。 
    
DT_SET_SELECTION 
  
> リストボックス内で選択が行われると、そのリストボックスのインデックス列がプロパティとして設定されます。 DT_SET_IMMEDIATE で常に使用されます。
    
このプロパティは、コントロールの[DTCTL](dtctl.md)構造の ulCtlFlags メンバに格納されます。 コントロールフラグのほとんどは、ユーザー入力を許可するすべてのコントロールに適用されます。編集コントロールにのみ適用されます。 ユーザー入力を許可しないコントロール (ボタン、ラベルなど) は、コントロールフラグに0を設定します。 
  
フラグの値の多くは、わかりやすいものになっています。 たとえば、コントロールに DT_REQUIRED が設定されている場合は、ダイアログボックスを閉じる前に値を設定する必要があります。 サービスプロバイダーは、 **imapiprop**の実装によって値を指定するか、またはユーザーが1つの値を入力できます。 DT_EDITABLE は、コントロールの値を変更できることを示します。 DT_MULTILINE では、編集コントロールの値が複数行にわたることができます。 
  
コントロールフラグによっては、意味がわかりません。 コントロールが DT_SET_IMMEDIATE フラグを設定すると、その値に加えられた変更は、ユーザーが新しいコントロールに移動した直後に影響を受けます。 MAPI は、プロパティインターフェイスの[imapiprop:: setprops](imapiprop-setprops.md)メソッドに対して、コントロールのプロパティに対して1回の呼び出しを行います。 これは既定の動作とは異なります。これは、ユーザーが **[OK** ] ボタンを選択するか、ダイアログボックスを閉じるまで、コントロールの値への変更を有効にするまでの時間を延期することです。 DT_SET_IMMEDIATE フラグは、多くの場合、表示テーブル通知と組み合わせて使用されます。 
  
次の表に、コントロールの種類と、各種類に対して設定できるフラグの値を示します。
  
|**Control**|**このプロパティの有効な値**|
|:-----|:-----|
|ボタン  <br/> |0である必要があります。  <br/> |
|チェック ボックス  <br/> |DT_EDITABLE、DT_SET_IMMEDIATE  <br/> |
|コンボ ボックス  <br/> |DT_EDITABLE、DT_REQUIRED、DT_SET_IMMEDIATE  <br/> |
|ドロップダウンリストボックス  <br/> |DT_EDITABLE、DT_SET_IMMEDIATE  <br/> |
|編集  <br/> |DT_ACCEPT_DBCS、DT_MULTILINE、DT_EDITABLE、DT_PASSWORD_EDIT、DT_REQUIRED、DT_SET_IMMEDIATE  <br/> |
|グループ ボックス  <br/> |0である必要があります。  <br/> |
|Label  <br/> |0である必要があります。  <br/> |
|リスト ボックス  <br/> |0である必要があります。  <br/> |
|[複数値] ドロップダウンリストボックス  <br/> |0である必要があります。  <br/> |
|複数値リストボックス  <br/> |0である必要があります。  <br/> |
|タブ付きページ  <br/> |0である必要があります。  <br/> |
|ラジオボタン  <br/> |0である必要があります。  <br/> |
   
## <a name="related-resources"></a>関連リソース

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

