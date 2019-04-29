---
title: ADRPARM
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRPARM
api_type:
- COM
ms.assetid: 35cd57b4-9901-456c-bf06-1f84e274eb4e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9663a25a50d914f47cff48124898d16318bbbc43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425898"
---
# <a name="adrparm"></a>ADRPARM

**適用対象**: Outlook 2013 | Outlook 2016 
  
[共通アドレス] ダイアログボックスの表示と動作について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRPARM
{
  ULONG cbABContEntryID;
  LPENTRYID lpABContEntryID;
  ULONG ulFlags;
  LPVOID lpReserved;
  ULONG ulHelpContext;
  LPSTR lpszHelpFileName;
  LPFNABSDI lpfnABSDI;
  LPFNDISMISS lpfnDismiss;
  LPVOID lpvDismissContext;
  LPSTR lpszCaption;
  LPSTR lpszNewEntryTitle;
  LPSTR lpszDestWellsTitle;
  ULONG cDestFields;
  ULONG nDestFieldFocus;
  LPSTR FAR *lppszDestTitles;
  ULONG FAR *lpulDestComps;
  LPSRestriction lpContRestriction;
  LPSRestriction lpHierRestriction;
} ADRPARM, FAR *LPADRPARM;

```

## <a name="members"></a>メンバー

**cbABContEntryID**
  
> **lpabコンテ entryid**によって指摘されたエントリ識別子のバイト数。
    
**lpabクレヨン entryid**
  
> [アドレス] ダイアログボックスに表示される受信者アドレスの初期のリストを提供するコンテナーのエントリ識別子へのポインター。
    
**ulFlags**
  
> さまざまな address ダイアログボックスオプションに関連付けられているフラグのビットマスク。 次のフラグを設定できます。
    
AB_RESOLVE
  
> [アドレス] ダイアログボックスを閉じた後、すべての名前を解決できるようにします。 名前解決プロセスの結果としてあいまいなエントリが表示された場合は、その解決のためにユーザーに確認するダイアログボックスが表示されます。 このフラグを設定すると、 [IAddrBook:: アドレス](iaddrbook-address.md)で返されるすべての名前が解決されることが保証されます。 
    
AB_SELECTONLY
  
> 受信者リストの1回限りのアドレスの作成を無効にします。 このフラグは、DIALOG_MODAL フラグが設定されている場合のように、ダイアログボックスがモーダルである場合にのみ使用されます。
    
ADDRESS_ONE
  
> ユーザーは、リストから複数の受信者の代わりに1人の受信者を選択できます。 このフラグは、 **cdestfields**が0で、ダイアログボックスがモーダルで、DIALOG_MODAL フラグが設定されている場合にのみ有効です。 
    
DIALOG_MODAL
  
> [共通アドレス] ダイアログボックスのモーダルバージョンが表示されます。 このフラグまたは DIALOG_SDI のいずれかを設定する必要があります。両方を設定することはできません。 
    
DIALOG_OPTIONS
  
> ダイアログボックスに [**送信オプション**] ボタンを表示します。 このフラグは、DIALOG_MODAL フラグが設定されている場合のように、ダイアログボックスがモーダルである場合にのみ使用されます。 
    
DIALOG_SDI
  
> [共通アドレス] ダイアログボックスのモードレスバージョンが表示されます。 このフラグまたは DIALOG_MODAL のいずれかを設定する必要があります。両方を設定することはできません。 Outlook 以外のクライアントでは、DIALOG_SDI フラグは無視され、ダイアログボックスのモーダルバージョンが表示されます。 そのため、 [IAddrBook:: Address](iaddrbook-address.md)の_lアウト uiparam_パラメーターでは、ハンドルへのポインターを想定しないようにする必要があります。
    
**lpreserved**
  
> 予約済み。0である必要があります。
    
**ulhelpcontext**
  
> ユーザーが [アドレス] ダイアログボックスの [ヘルプ] ボタンをクリックしたときに最初に表示される**ヘルプ**内のコンテキストを指定します。 
    
**lpszhelpfilename**
  
> [アドレス] ダイアログボックスに関連付けられたヘルプファイルの名前へのポインター。 **lpszhelpfilename**メンバーは、Windows **WinHelp**関数を呼び出すために**ulhelpcontext**と共に使用されます。 
    
**lpfnABSDI**
  
> [ACCELERATEABSDI](accelerateabsdi.md) prototype または NULL に基づく MAPI 関数へのポインター。 このメンバーは、DIALOG_SDI フラグが設定されている場合にのみ、ダイアログボックスのモードレスバージョンに適用されます。 [IAddrBook:: Address](iaddrbook-address.md)に渡す**ADRPARM**構造を構築しているクライアントは、常に**lpfnABSDI**メンバーを NULL に設定する必要があります。 DIALOG_SDI フラグが設定されている場合、MAPI は返される前に有効な関数に設定します。 クライアントは、メッセージループでこの関数を呼び出して、[アドレス帳] ダイアログボックスのアクセラレータが機能することを確認します。 ダイアログボックスが閉じられ、MAPI が**lpfnDismiss**メンバーによって示される関数を呼び出すと、クライアントは、メッセージループから**ACCELERATEABSDI**関数をアンフックする必要があります。 
    
**lpfnDismiss**
  
> [DISMISSMODELESS](dismissmodeless.md) prototype または NULL に基づく関数へのポインター。 このメンバーは、DIALOG_SDI フラグが設定されている場合にのみ、ダイアログボックスのモードレスバージョンにのみ適用されます。 ユーザーが [モードレスアドレス] ダイアログボックスを閉じたときに MAPI が**DISMISSMODELESS**関数を呼び出し、 **IAddrBook::** を呼び出していることをクライアントに通知します。このダイアログボックスはアクティブではなくなっています。 
    
**lpvDismissContext**
  
> **lpfnDismiss**メンバーが指す**DISMISSMODELESS**関数に渡されるコンテキスト情報へのポインター。 このメンバーは、DIALOG_SDI フラグが設定されている場合のように、ダイアログボックスのモードレスバージョンにのみ適用されます。 
    
**lpszcaption**
  
> [共通アドレス] ダイアログボックスのタイトルとして使用するテキストへのポインター。
    
**lpsznewentrytitle**
  
> [**新しいエントリ**] ダイアログボックスまたは別のダイアログボックスを起動するボタンのボタンラベルとして使用するテキストへのポインター。 
    
**lpszDestWellsTitle**
  
> [宛先] テキストボックスコントロールのタイトルとして使用するテキストへのポインターです。これは、[共通アドレス] ダイアログボックスのモーダルバージョンに表示されます。 このメンバーは、モードレスダイアログボックスでは使用されません。 
    
**cdestfields**
  
> [アドレス] ダイアログボックスのモーダルバージョンに含まれる受信者テキストボックスコントロールの数、またはダイアログボックスがモードレスの場合は0になります。 [アドレス] ダイアログボックスは、次の条件が満たされている場合にのみブラウズ用に開かれます。 
    
  - **cdestfields**メンバーが0に設定されています。 
    
  - DIALOG_BOX フラグが設定されています。
    
  - ADDRESS_ONE フラグが設定されていません。
    
  **cdestfields**を0xffffffff に設定すると、MAPI は受信者テキストボックスコントロールの既定の数を作成する必要があります。 この場合、 **lppszdesttitles**メンバーおよび**lアウト destカンプ**メンバーは NULL である必要があります。 
    
**ndestfieldfocus**
  
> モーダルバージョンのダイアログボックスが表示されるときに最初にフォーカスする必要があるテキストボックスコントロールを示します。 この値は、0から**cdestfields**から1を引いた値までの範囲にする必要があります。 
    
**lppszdesttitles**
  
> [アドレス] ダイアログボックスのモーダルバージョンに表示される各テキストボックスコントロールに関連付けられているボタンのラベルの配列へのポインター。 **cdestfields**メンバーの値は、配列に含まれているラベルの数を示します。 **lppszdesttitles**メンバーが NULL の場合、 **Address**メソッドは既定のタイトルを使用します。 
    
**lアウト destカンプ**
  
> 各テキストボックスコントロールに関連付けられている、MAPI_TO、MAPI_CC、MAPI_BCC などの受信者の種類の値の配列へのポインター。 **cdestfields**メンバーの値は、配列に含まれる受信者の種類の数を示します。 **lPR_RECIPIENT_TYPE destカンプ**が指す値を使用して、各受信者の**** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティを設定できます。 **lpuldestcomps**メンバーが NULL の場合、 **Address**メソッドは既定の受信者の種類を使用します。 
    
**lpコンテ制限**
  
> ダイアログボックスに表示できるアドレスエントリの種類を制限する[srestriction](srestriction.md)構造体へのポインター。 
    
**lpHierRestriction**
  
> ダイアログボックスに表示されるアドレスエントリを提供できるアドレス帳のコンテナーを制限する**srestriction**構造体へのポインター。 
    
## <a name="remarks"></a>注釈

**ADRPARM**構造体は、クライアントとサービスプロバイダーによって、MAPI の共通アドレスダイアログボックスの外観と動作を制御するために使用されます。 [アドレス] ダイアログボックスには、モードレスとモーダルの2種類があります。 **ADRPARM**構造体のメンバーの中には、ダイアログボックスの両方のバージョンに適用されるものもありますが、一部は2つのバージョンのどちらかにのみ適用されます。 次の表では、 **ADRPARM**構造体のメンバーを、共通のアドレスダイアログボックスで使用する方法に関連しています。 
  
|ADRPARM メンバー|ダイアログボックスの種類|
|:-----|:-----|
|**cbABContEntryID**および**lpabクレヨン entryid** <br/> |モーダルおよびモードレス  <br/> |
|**ulFlags** <br/> |モーダルおよびモードレス  <br/> |
|**lpreserved** <br/> |モーダルおよびモードレス  <br/> |
|**ulhelpcontext**と**lpszhelpfilename** <br/> |モーダルおよびモードレス  <br/> |
|**lpfnABSDI** <br/> |Modeless  <br/> |
|**lpfnDismiss**および**lpvDismissContext** <br/> |Modeless  <br/> |
|**lpszcaption** <br/> |モーダルおよびモードレス  <br/> |
|**lpsznewentrytitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**、 **cdestfields**、 **ndestfieldfocus**、 **lppszdesttitles**、 **lindexdestカンプ** <br/> |Modal  <br/> |
|**lpコンテ制限** <br/> |モーダルおよびモードレス  <br/> |
|**lpHierRestriction** <br/> |モーダルおよびモードレス  <br/> |
   
モードレスダイアログボックスは、1つまたは複数のアドレス帳コンテナーからのエントリを読み取り専用で表示します。 このダイアログボックスでは、選択したコンテナーからのすべてのエントリを表示することも、制限によって設定された条件に一致するエントリとコンテナーのみに制限することもできます。 **lpコンテ制限**によって参照されるコンテンツ制限によって、表示されるエントリの種類と、 **lpHierRestriction**によって示される階層制限によって、エントリを提供するコンテナーを制限できます。 ダイアログボックスが閉じられたときに発信者に通知するために、MAPI は、 [DISMISSMODELESS](dismissmodeless.md)プロトタイプに一致する呼び出し元によって提供される関数を呼び出します。 [ACCELERATEABSDI](accelerateabsdi.md)プロトタイプに一致するもう1つの関数は MAPI によって提供され、Windows メッセージループで呼び出し元によって呼び出され、キーボードショートカットの動作を容易にします。 クライアントが[IAddrBook:: アドレス](iaddrbook-address.md)を呼び出したとき、またはサービスプロバイダーが[imapisupport:: address](imapisupport-address.md)を呼び出したときに、モードレスバージョンの [MAPI アドレス] ダイアログボックスが表示されることがあります。 
  
モーダルダイアログボックスは、1つまたは複数のコンテナーからのエントリを読み取り/書き込みで表示します。 この内容は、 **lpコンテ制限**および**lpHierRestriction**メンバーで設定された制限によって、モードレスバージョンと同じ方法で影響を受ける可能性があります。 コンテナーエントリを表示するリストボックスに加えて、モーダルダイアログボックスには、ユーザーによって選択されたエントリを保持するためのテキストボックスコントロールを 1 ~ 3 個まで含めることができます。 各編集コントロールは、MAPI_TO などの特定の受信者の種類または**PR_RECIPIENT_TYPE**プロパティに関連付けられます。 [モーダルアドレス] ダイアログボックスを表示するには、いずれかの**アドレス**方法を使用するか、クライアントが[IAddrBook](iaddrbook-details.md)を呼び出すときに、etails とサービスプロバイダーの呼び出し[imapisupport::D etails](imapisupport-details.md)を使用します。 
  
この図には2つのテキストボックスコントロールが含まれています。このダイアログボックスの表示を制御する**ADRPARM**構造体の**cdestfields**メンバーは2に設定されています。 **ndestfieldfocus**メンバーが0に設定されているため、最初のコントロールには最初のフォーカスがあります。 
  
**lpsznewentrytitle**メンバーは、選択時にボタンラベルのテキストをポイントすると、追加のダイアログボックスが表示されます。 通常、モーダルダイアログボックスの図に示されているように、ボタンに [**新規**] というラベルが付けられ、表示されるダイアログボックスに、プロファイル内の任意のアドレス帳プロバイダーで作成できるアドレスの種類が一覧表示されます。 クライアントは[IAddrBook:: newentry](iaddrbook-newentry.md)を呼び出し、 _cbeidnewentrytpl_パラメーターに0を渡し、ユーザーがボタンを選択したときに_lpeidnewentrytpl_パラメーターに NULL を渡すことによって、この**新しいエントリ**のダイアログボックスが表示されます。 このダイアログボックスに含まれる情報は、MAPI の1回限りのテーブルから取得されます。 
  
このダイアログボックスのすべてのエントリは、特定の種類のアドレスを作成するために必要なデータを入力するためのテンプレートに関連付けられています。 ほとんどのアドレス帳プロバイダーは、作成できるアドレスエントリの種類ごとに1つのテンプレートを提供します。 このダイアログボックスからユーザーが選択を行うと、MAPI には対応するテンプレートが表示されます。
  
**ADRPARM**構造体の**ulflags**メンバーの最上位4ビットには、 **ADRPARM**構造のバージョンを識別するバージョン番号が含まれています。 現在のバージョンは 0 (ゼロ) または ADRPARM_HELP_CTX です。 現在の MAPI の実装は、ゼロ以外の構造体のバージョンでは失敗します。 
  
将来の構造のバージョンは、まったく異なる場合があります。これらは、バージョン0の構造をサポートしていない場合があります。 **ulflags**メンバーからバージョン番号を抽出し、定義されたフラグと組み合わせるために、次のマクロが提供されています。 
  
- **GET_ADRPARM_VERSION**(_ulflags_) 
- **SET_ADRPARM_VERSION**(_ulflags_、_ ulflags _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>関連項目

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [MAPI の構造](mapi-structures.md)

