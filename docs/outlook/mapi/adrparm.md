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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 560cae5e8a3d73d80a4907fd0fec43b389ef9fc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572026"
---
# <a name="adrparm"></a>ADRPARM

**適用されます**: Outlook 2013 |Outlook 2016 
  
表示と共通のアドレス] ダイアログ ボックスの動作について説明します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
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

## <a name="members"></a>Members

**cbABContEntryID**
  
> **LpABContEntryID**で示されるエントリの識別子のバイト数をカウントします。
    
**lpABContEntryID**
  
> 最初に、[アドレス] ダイアログ ボックスに表示される受信者のアドレスのリストを提供するコンテナーのエントリの識別子へのポインター。
    
**ulFlags**
  
> アドレス] ダイアログ ボックスの各種のオプションに関連付けられたフラグのビットマスクです。 次のフラグを設定することができます。
    
AB_RESOLVE
  
> [アドレス] ダイアログ ボックスが閉じられた後に解決されるすべての名前を有効にします。 名前解決の処理に起因するあいまいなエントリがある場合は、それらを解決するにはユーザーの入力を求めるダイアログ ボックスが表示されます。 確実に解決されるすべての[IAddrBook::Address](iaddrbook-address.md)によって返される名前が設定されます。 
    
AB_SELECTONLY
  
> 受信者の一覧については、一時アドレスの作成を無効にします。 DIALOG_MODAL フラグが設定されている中で示されるように、ダイアログ ボックスはモーダルで場合にのみ、このフラグが使用されます。
    
ADDRESS_ONE
  
> ユーザーは、一覧から複数の受信者ではなく正確に 1 つの受信者を選択できます。 このフラグは、 **cDestFields**がゼロで、DIALOG_MODAL フラグが設定されている中で示されるように、ダイアログ ボックスはモーダルで場合にのみに有効です。 
    
DIALOG_MODAL
  
> モーダルに表示される共通のアドレス] ダイアログ ボックスのバージョンが発生します。 このフラグまたは DIALOG_SDI のいずれかを設定する必要があります。それら両方は設定できません。 
    
DIALOG_OPTIONS
  
> ダイアログ ボックスに表示される**オプションの送信**] ボタンが発生します。 DIALOG_MODAL フラグが設定されている中で示されるように、ダイアログ ボックスはモーダルで場合にのみ、このフラグが使用されます。 
    
DIALOG_SDI
  
> モードレスに表示される共通のアドレス] ダイアログ ボックスのバージョンが発生します。 このフラグまたは DIALOG_MODAL のいずれかを設定する必要があります。それら両方は設定できません。 DIALOG_SDI フラグは無視されます、Outlook 以外のクライアントと、ダイアログ ボックスのモーダル バージョンが表示されます。 その結果、ハンドルへのポインターを期待していない[IAddrBook::Address](iaddrbook-address.md)の_lpulUIParam_パラメーターにします。
    
**lpReserved**
  
> 予約済み、0 でなければなりません。
    
**ulHelpContext**
  
> **ヘルプ**を最初に表示されますユーザーが、[アドレス] ダイアログ ボックスで [ヘルプ] ボタンをクリックしたときにコンテキストを指定します。 
    
**lpszHelpFileName**
  
> [アドレス] ダイアログ ボックスに関連付けられるヘルプ ファイルの名前へのポインター。 **UlHelpContext**とは、 **lpszHelpFileName**メンバーを使用して、Windows**ヘルプ**関数を呼び出します。 
    
**lpfnABSDI**
  
> [ACCELERATEABSDI](accelerateabsdi.md)のプロトタイプには MAPI 関数へのポインター。 このメンバーは、モードレス ダイアログ ボックスでのみのバージョンに適用されます DIALOG_SDI フラグが設定されている中で示されるようにします。 [IAddrBook::Address](iaddrbook-address.md)に渡すための**ADRPARM**構造体を構築するクライアントは、 **lpfnABSDI**メンバーを NULL に設定する必要があります常に。 DIALOG_SDI フラグが設定されている場合 MAPI は後でその設定に有効な関数を返す前に。 クライアントは、アドレスでアクセラレータが] ダイアログ ボックスの作業を予約するかどうかを確認するメッセージ ループ内からこの関数を呼び出します。 ダイアログ ボックスを閉じるし、MAPI は、 **lpfnDismiss**のメンバーで指定された関数を呼び出す、クライアントする必要があります、メッセージ ループから**ACCELERATEABSDI**関数を外します。 
    
**lpfnDismiss**
  
> [DISMISSMODELESS](dismissmodeless.md)のプロトタイプでは関数へのポインター。 このメンバーは、モードレス ダイアログ ボックスでのみのバージョンにのみ適用されます DIALOG_SDI フラグが設定されている中で示されるようにします。 MAPI 関数を呼び出す**DISMISSMODELESS**ユーザーが、アドレスのモードレス ダイアログ ボックスを閉じると、 **IAddrBook::Address**ダイアログ ボックスがアクティブではないことを呼び出すクライアントに通知します。 
    
**lpvDismissContext**
  
> **LpfnDismiss**メンバーが指す、 **DISMISSMODELESS**関数に渡されるコンテキスト情報へのポインターです。 このメンバーは、DIALOG_SDI フラグが設定されている中で示されるように、モードレス ダイアログ ボックスのバージョンにのみ適用されます。 
    
**lpszCaption**
  
> 共通のアドレス] ダイアログ ボックスのタイトルとして使用する文字列へのポインター。
    
**lpszNewEntryTitle**
  
> **[新しいエントリ**] ダイアログ ボックスまたは別のダイアログ ボックスのいずれかを起動するボタンのボタンのラベルとして使用する文字列へのポインター。 
    
**lpszDestWellsTitle**
  
> 共通のアドレス] ダイアログ ボックスのモーダル バージョンに表示される受信者のテキスト ボックス コントロールのタイトルとして使用する文字列へのポインター。 モードレス ダイアログ ボックスのこのメンバーは使用されません。 
    
**cDestFields**
  
> 受信者内のテキスト ボックス コントロール、[アドレス] ダイアログ ボックスまたはダイアログ ボックスがモードレスの場合にゼロのモーダル バージョンの数です。 [アドレス] ダイアログ ボックスは、次の条件に該当する場合にのみを参照するために開いています。 
    
  - **CDestFields**メンバーは、0 に設定されています。 
    
  - DIALOG_BOX フラグが設定されています。
    
  - ADDRESS_ONE フラグが設定されていません。
    
  **CDestFields**を 0 XFFFFFFFF に設定すると、MAPI を作成するように受信者のテキストの既定の数] ボックスのコントロールを意味します。 この例では、 **lppszDestTitles**と**lpulDestComps**のメンバーは NULL にする必要があります。 
    
**nDestFieldFocus**
  
> モーダル ダイアログ ボックスのバージョンが表示されたら、初期フォーカスを持っている必要がありますが、特定のテキスト ボックス コントロールを示します。 この値は、0 から 1 を引いた**cDestFields**の値の間にする必要があります。 
    
**lppszDestTitles**
  
> [アドレス] ダイアログ ボックスのモーダル バージョンで表示されているテキスト ボックス コントロールのそれぞれに関連付けられたボタンのラベルの配列へのポインター。 **CDestFields**メンバーの値は、配列に含まれているラベルの数を示します。 **LppszDestTitles**メンバーが NULL の場合は、**アドレス**のメソッドは、既定のタイトルを使用します。 
    
**lpulDestComps**
  
> 各テキスト ボックス コントロールに関連付けられている MAPI_TO、MAPI_CC、MAPI_BCC などの受信者の種類の値の配列へのポインター。 **CDestFields**メンバーの値は、配列に含まれる受信者の種類の数を示します。 **LpulDestComps**が指す値は、各受信者の**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) のプロパティを設定するのには使用できます。 **LpulDestComps**メンバーが NULL の場合は、**アドレス**のメソッドは、既定の受信者の種類を使用します。 
    
**lpContRestriction**
  
> ダイアログ ボックスで表示されるアドレス エントリの種類を制限する[SRestriction](srestriction.md)構造体へのポインター。 
    
**lpHierRestriction**
  
> ダイアログ ボックスに表示されるアドレスのエントリを提供できるアドレス帳コンテナーを制限する**SRestriction**構造体へのポインター。 
    
## <a name="remarks"></a>注釈

コモン アドレス] ダイアログ ボックスの動作と外観を制御するクライアントとサービス ・ プロバイダーによって使用されるは、 **ADRPARM**構造体です。 [アドレス] ダイアログ ボックスの 2 つの種類があります: モードレスとモーダルです。 **ADRPARM**構造体のメンバーのいくつかのダイアログ ボックスの両方のバージョンに適用しますが、いくつかは、2 つのバージョンのいずれかにのみ適用します。 次の表には、共通のアドレス] ダイアログ ボックスで、使用する**ADRPARM**構造体のメンバーが関連しています。 
  
|ADRPARM メンバー|ダイアログ ボックスの種類|
|:-----|:-----|
|**cbABContEntryID**と**lpABContEntryID** <br/> |モーダルおよびモードレス  <br/> |
|**ulFlags** <br/> |モーダルおよびモードレス  <br/> |
|**lpReserved** <br/> |モーダルおよびモードレス  <br/> |
|**ulHelpContext**と**lpszHelpFileName** <br/> |モーダルおよびモードレス  <br/> |
|**lpfnABSDI** <br/> |Modeless  <br/> |
|**lpfnDismiss**と**lpvDismissContext** <br/> |Modeless  <br/> |
|**lpszCaption** <br/> |モーダルおよびモードレス  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**、 **cDestFields**、 **nDestFieldFocus**、 **lppszDestTitles**、および**lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |モーダルおよびモードレス  <br/> |
|**lpHierRestriction** <br/> |モーダルおよびモードレス  <br/> |
   
モードレス ダイアログ ボックスは、1 つまたは複数のアドレス帳コンテナーからのエントリの読み取り専用表示です。 ダイアログ ボックスでは、選択したコンテナーからすべてのエントリを表示したり、エントリと、制限が設定した基準に一致するコンテナーのみに限定することができます。 **LpContRestriction**が指す内容の制限が表示されるエントリの種類を制限し、 **lpHierRestriction**で示される階層の制限は、コンテナーのエントリを提供することを制限できます。 ダイアログ ボックスを終了したときに呼び出し元に通知をするには、MAPI は、 [DISMISSMODELESS](dismissmodeless.md)のプロトタイプに一致する呼び出し元によって提供される関数を呼び出します。 [ACCELERATEABSDI](accelerateabsdi.md)プロトタイプに一致する別の関数は MAPI によって提供され、キーボード ショート カットの作業を容易にする Windows メッセージ ループの呼び出し元によって呼び出されます。 クライアントは、 [IAddrBook::Address](iaddrbook-address.md)を呼び出すとき、またはサービス プロバイダーは、 [IMAPISupport::Address](imapisupport-address.md)を呼び出すと、モードレスのバージョンの MAPI アドレス] ダイアログ ボックスを表示できます。 
  
モーダル ダイアログ ボックスは、1 つまたは複数のコンテナーからのエントリの読み取り/書き込みの表示です。 モードレス バージョンの制限を設定**lpContRestriction**と**lpHierRestriction**のメンバーと同様にその内容が適用されます。 コンテナーのエントリを表示するボックスの一覧のほか、モーダル ダイアログ ボックスがユーザーによって選択されたエントリを保持するために、1 つと 3 つのテキスト ボックス コントロールの間で含めることができます。 各エディット コントロールは、特定の受信者の種類や MAPI_TO などの**PR_RECIPIENT_TYPE**プロパティに関連付けられます。 クライアントは、 [IAddrBook::Details](iaddrbook-details.md)を呼び出すし、サービス プロバイダーは、 [IMAPISupport::Details](imapisupport-details.md)を呼び出すとき、または**アドレス**の方法のいずれかで、作業ウィンドウ固定のアドレス] ダイアログ ボックスを表示できます。 
  
**CDestFields** 、 **ADRPARM**構造体のメンバーは、このダイアログ ボックスの表示を制御することが 2 に設定されているために、この図には 2 つのテキスト ボックス コントロールが含まれます。 最初のコントロールでは、 **nDestFieldFocus**メンバーは 0 に設定されているために初期フォーカスがあります。 
  
**LpszNewEntryTitle**メンバーを選択すると、追加のダイアログ ボックスを表示すると、ボタンのラベルのテキストをポイントします。 通常は、ボタンの**新しい**ラベルは、図のように、モーダル ダイアログ ボックスのし、表示されるダイアログ ボックスのすべてのプロファイルで、アドレス帳プロバイダーのいずれかで作成可能なアドレスの種類の一覧が表示されます。 クライアントには、 [IAddrBook::NewEntry](iaddrbook-newentry.md)を呼び出すと、ユーザーがボタンを選択した場合、 _cbEidNewEntryTpl_パラメーターの 0 と_lpEidNewEntryTpl_のパラメーターに NULL を渡すことによって表示されるこの**新しいエントリ**のダイアログ ボックスがあります。 このダイアログ ボックスに含まれる情報は、MAPI の一時テーブルから取得されます。 
  
このダイアログ ボックス内のすべてのエントリは、特定の種類のアドレスを作成するために必要なデータを入力するためのテンプレートに関連付けられます。 ほとんどのアドレス帳プロバイダーでは、アドレスのエントリを作成することのすべての種類の 1 つのテンプレートを提供します。 このダイアログ ボックスから選択を行うと、MAPI には、対応するテンプレートが表示されます。
  
**ADRPARM**構造体の**ulFlags**メンバーの最上位 4 ビットには、 **ADRPARM**構造体のバージョンを識別するバージョン番号が含まれています。 現在のバージョンは、0 (ゼロ) または ADRPARM_HELP_CTX。 MAPI の現在の実装は、0 以外の構造体のすべてのバージョンで失敗します。 
  
構造体の将来のバージョンが完全に別の可能性があります。バージョン 0 の構造体ができません。 **UlFlags**メンバーからバージョン番号を抽出するため、定義済みのフラグを組み合わせることで、次のマクロが用意されています。 
  
- **GET_ADRPARM_VERSION**(_ulFlags_) 
- **SET_ADRPARM_VERSION**(_ulFlags_、_ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>関連項目

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [MAPI の構造](mapi-structures.md)

