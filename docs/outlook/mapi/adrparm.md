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
  
[共通アドレス] ダイアログ ボックスの表示と動作について説明します。 
  
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
  
> **lpABContEntryID** が指すエントリ識別子内のバイト数です。
    
**lpABContEntryID**
  
> [アドレス] ダイアログ ボックスに表示される受信者アドレスの最初の一覧を提供するコンテナーのエントリ識別子へのポインター。
    
**ulFlags**
  
> さまざまなアドレス ダイアログ ボックスオプションに関連付けられたフラグのビットマスク。 次のフラグを設定できます。
    
AB_RESOLVE
  
> [アドレス] ダイアログ ボックスを閉じた後で、すべての名前を解決できます。 名前解決プロセスの結果としてあいまいなエントリがある場合は、ユーザーに解決の助けを求めるダイアログ ボックスが表示されます。 このフラグを設定すると [、IAddrBook::Address](iaddrbook-address.md) によって返される名前はすべて解決されます。 
    
AB_SELECTONLY
  
> 受信者リストの一時アドレスの作成を無効にします。 このフラグは、ダイアログ ボックスがモーダルである場合にのみ使用されます。設定されているフラグDIALOG_MODAL示します。
    
ADDRESS_ONE
  
> ユーザーは、リストから複数の受信者ではなく、正確に 1 つの受信者を選択できます。 このフラグは **、cDestFields** が 0 で、ダイアログ ボックスがモーダルである場合にのみ有効です。設定されているフラグDIALOG_MODAL示されます。 
    
DIALOG_MODAL
  
> 共通アドレス ダイアログ ボックスのモーダル バージョンが表示されます。 このフラグまたは設定DIALOG_SDI設定する必要があります。両方を設定することはできません。 
    
DIALOG_OPTIONS
  
> ダイアログ ボックスに **[オプション** の送信] ボタンを表示します。 このフラグは、ダイアログ ボックスがモーダルである場合にのみ使用されます。設定されているフラグDIALOG_MODAL示します。 
    
DIALOG_SDI
  
> [共通アドレス] ダイアログ ボックスのモードレス バージョンが表示されます。 このフラグまたは設定DIALOG_MODAL設定する必要があります。両方を設定することはできません。 クライアントDIALOG_SDIの Outlook場合、DIALOG_SDIフラグは無視され、ダイアログ ボックスのモーダル バージョンが表示されます。 したがって [、IAddrBook::Address](iaddrbook-address.md)の _lpulUIParam_ パラメーターでは、ハンドルへのポインターを予期しない必要があります。
    
**lpReserved**
  
> 予約済みで、ゼロである必要があります。
    
**ulHelpContext**
  
> ユーザーが [アドレス **]** ダイアログ ボックスの [ヘルプ] ボタンをクリックすると最初に表示されるヘルプ内のコンテキストを指定します。 
    
**lpszHelpFileName**
  
> アドレス ダイアログ ボックスに関連付けられるヘルプ ファイルの名前へのポインター。 **lpszHelpFileName** メンバーは **、ulHelpContext** と共に使用して、winHelp 関数Windows **呼び出** します。 
    
**lpfnABSDI**
  
> [ACCELERATEABSDI](accelerateabsdi.md)プロトタイプまたは NULL に基づく MAPI 関数へのポインター。 このメンバーは、設定されているオプション フラグで示されているモードレス DIALOG_SDIダイアログ ボックスにのみ適用されます。 [IAddrBook::Address](iaddrbook-address.md)に渡す **ADRPARM** 構造を構築するクライアントは、常に **lpfnABSDI** メンバーを NULL に設定する必要があります。 このフラグDIALOG_SDI設定すると、MAPI は返す前に有効な関数に設定されます。 クライアントは、メッセージ ループからこの関数を呼び出して、アドレス帳ダイアログ ボックスのアクセラレータが機能する必要があります。 ダイアログ ボックスが閉じ、MAPI が **lpfnDismiss** メンバーが指す関数を呼び出す場合、クライアントはメッセージ ループから **ACCELERATEABSDI** 関数を解除する必要があります。 
    
**lpfnDismiss**
  
> [DISMISSMODELESS](dismissmodeless.md)プロトタイプまたは NULL に基づく関数へのポインター。 このメンバーは、設定されているオプション フラグで示されているとおり、ダイアログ ボックスのモードレス バージョンにのみ適用されます。DIALOG_SDIします。 MAPI は、ユーザーがモードレス アドレス ダイアログ ボックスを閉じ、ダイアログ ボックスがアクティブでなくなった **IAddrBook::Address** を呼び出すクライアントに通知するときに **DISMISSMODELESS** 関数を呼び出します。 
    
**lpvDismissContext**
  
> **lpfnDismiss** メンバーが指す **DISMISSMODELESS** 関数に渡されるコンテキスト情報へのポインター。 このメンバーは、設定されているオプション フラグで示されているモードレス DIALOG_SDIダイアログ ボックスにのみ適用されます。 
    
**lpszCaption**
  
> 共通アドレス ダイアログ ボックスのタイトルとして使用するテキストへのポインター。
    
**lpszNewEntryTitle**
  
> [新しいエントリ] ダイアログ ボックスまたは別のダイアログ ボックスを呼び出すボタンのボタン ラベルとして使用するテキストへのポインター。 
    
**lpszDestWellsTitle**
  
> 共通アドレス ダイアログ ボックスのモーダル バージョンに表示できる受信者テキスト ボックス コントロールのタイトルとして使用するテキストへのポインター。 このメンバーは、モードレス ダイアログ ボックスには使用されません。 
    
**cDestFields**
  
> モーダル バージョンのアドレス ダイアログ ボックスの受信者テキスト ボックス コントロールの数、またはダイアログ ボックスがモードレスの場合は 0。 [アドレス] ダイアログ ボックスは、次の条件が満たされている場合にのみ参照用に開きます。 
    
  - **cDestFields メンバーは** 0 に設定されます。 
    
  - このDIALOG_BOXが設定されます。
    
  - このADDRESS_ONEフラグは設定されていない。
    
  **cDestFields を 0XFFFFFFFF** すると、MAPI は受信者テキスト ボックス コントロールの既定の数を作成する必要があります。 この場合 **、lppszDestTitles および** **lpulDestComps メンバー** は NULL である必要があります。 
    
**nDestFieldFocus**
  
> ダイアログ ボックスのモーダル バージョンが表示される場合に、最初のフォーカスを持つ必要がある特定のテキスト ボックス コントロールを示します。 この値は、0 から **cDestFields** から 1 を引いた値の間である必要があります。 
    
**lppszDestTitles**
  
> モーダル バージョンのアドレス ダイアログ ボックスに表示される各テキスト ボックス コントロールに関連付けられたボタンのラベルの配列へのポインター。 **cDestFields メンバーの値** は、配列に含まれるラベルの数を示します。 **lppszDestTitles メンバー** が NULL の場合 **、Address** メソッドは既定のタイトルを使用します。 
    
**lpulDestComps**
  
> 各テキスト ボックス コントロールに関連付けられている MAPI_TO、MAPI_CC、MAPI_BCC など、受信者の種類の値の配列へのポインター。 **CDestFields** メンバーの値は、配列に含まれる受信者の種類の数を示します。 **lpulDestComps** が指す値を使用して、各受信者の PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティを設定できます。 **lpulDestComps メンバー** が NULL の場合 **、Address** メソッドは既定の受信者の種類を使用します。 
    
**lpContRestriction**
  
> ダイアログ ボックスに表示できるアドレス エントリの種類を制限する [SRestriction](srestriction.md) 構造へのポインター。 
    
**lpHierRestriction**
  
> ダイアログ ボックスに表示するアドレス エントリを指定できるアドレス帳コンテナーを制限する **SRestriction** 構造へのポインター。 
    
## <a name="remarks"></a>注釈

**ADRPARM 構造** は、MAPI 共通アドレス ダイアログ ボックスの外観と動作を制御するために、クライアントおよびサービス プロバイダーによって使用されます。 [アドレス] ダイアログ ボックスには、モードレスとモーダルの 2 種類があります。 **ADRPARM** 構造のメンバーの一部は、ダイアログ ボックスの両方のバージョンに適用されますが、一部のメンバーは 2 つのバージョンの 1 にのみ適用されます。 次の表は **、ADRPARM** 構造体のメンバーと、共通のアドレス ダイアログ ボックスでの使用に関する説明です。 
  
|ADRPARM メンバー|ダイアログ ボックスの種類|
|:-----|:-----|
|**cbABContEntryID** と **lpABContEntryID** <br/> |モーダルとモードレス  <br/> |
|**ulFlags** <br/> |モーダルとモードレス  <br/> |
|**lpReserved** <br/> |モーダルとモードレス  <br/> |
|**ulHelpContext** と **lpszHelpFileName** <br/> |モーダルとモードレス  <br/> |
|**lpfnABSDI** <br/> |Modeless  <br/> |
|**lpfnDismiss と** **lpvDismissContext** <br/> |Modeless  <br/> |
|**lpszCaption** <br/> |モーダルとモードレス  <br/> |
|**lpszNewEntryTitle** <br/> |Modal  <br/> |
|**lpszDestWellsTitle**、 **cDestFields**、 **nDestFieldFocus**、 **lppszDestTitles**、 **および lpulDestComps** <br/> |Modal  <br/> |
|**lpContRestriction** <br/> |モーダルとモードレス  <br/> |
|**lpHierRestriction** <br/> |モーダルとモードレス  <br/> |
   
モードレス ダイアログ ボックスは、1 つ以上のアドレス帳コンテナーからのエントリの読み取り専用表示です。 ダイアログ ボックスには、選択したコンテナーのすべてのエントリを表示するか、制限によって確立された条件に一致するエントリとコンテナーのみを表示できます。 **lpContRestriction** が指すコンテンツ制限は、表示されるエントリの種類を制限し **、lpHierRestriction** が指す階層制限によって、エントリを提供するコンテナーを制限できます。 ダイアログ ボックスが閉じらされた場合に呼び出し元に通知するために、MAPI は [、DISMISSMODELESS](dismissmodeless.md) プロトタイプに一致する呼び出し元によって提供される関数を呼び出します。 [ACCELERATEABSDI](accelerateabsdi.md)プロトタイプに一致する別の関数は、MAPI によって提供され、Windows メッセージ ループ内の呼び出し元によって呼び出され、キーボード ショートカットの作業を容易にします。 クライアントが [IAddrBook::Address](iaddrbook-address.md) を呼び出す場合、またはサービス プロバイダーが [IMAPISupport::Address](imapisupport-address.md)を呼び出す場合は、モードレスバージョンの MAPI アドレス ダイアログ ボックスを表示できます。 
  
モーダル ダイアログ ボックスは、1 つ以上のコンテナーからのエントリの読み取り/書き込み表示です。 その内容は **、lpContRestriction** および **lpHierRestriction** メンバーで設定された制限によって、モードレス バージョンと同じ方法で影響を受ける可能性があります。 コンテナー エントリを表示するリスト ボックスに加えて、モーダル ダイアログ ボックスには、ユーザーが選択したエントリを保持するための 1 ~ 3 つのテキスト ボックス コントロールを含めできます。 各編集コントロールは、特定の受信者の種類や **PR_RECIPIENT_TYPEプロパティ** (MAPI_TO) に関連付MAPI_TO。 モーダル アドレス ダイアログ ボックスは **、Address** メソッドまたはクライアントが [IAddrBook::D etails](iaddrbook-details.md) とサービス プロバイダーが [IMAPISupport::D etails](imapisupport-details.md)を呼び出す場合に表示できます。 
  
この図には、このダイアログ ボックスの表示を制御する **ADRPARM** 構造体 **の cDestFields** メンバーが 2 に設定されているので、2 つのテキスト ボックス コントロールが含まれています。 **nDestFieldFocus** メンバーが 0 に設定されている場合、最初のコントロールには最初のフォーカスがあります。 
  
**lpszNewEntryTitle** メンバーは、ボタン ラベルを選択すると、追加のダイアログ ボックスが表示されるテキストをポイントします。 通常、モーダル ダイアログ ボックスの図に示すように、ボタンには [新規]というラベルが付き、表示されるダイアログ ボックスには、プロファイル内のアドレス帳プロバイダーが作成できるすべての種類のアドレスが一覧表示されます。 クライアントは [、IAddrBook::NewEntry](iaddrbook-newentry.md)を呼び出し _、cbEidNewEntryTpl_ パラメーターに 0 を渡し、ユーザーがボタンを選択すると _lpEidNewEntryTpl_ パラメーターに NULL を渡すことによって、この [新しいエントリ] ダイアログ ボックスを表示します。  このダイアログ ボックスに含まれる情報は、MAPI の一時テーブルから取得されます。 
  
このダイアログ ボックス内のすべてのエントリは、特定の種類のアドレスを作成するために必要なデータを入力するテンプレートに関連付けられている。 ほとんどのアドレス帳プロバイダーは、作成できるアドレスエントリのすべての種類に対して 1 つのテンプレートを提供します。 ユーザーがこのダイアログ ボックスから選択すると、対応するテンプレートが MAPI に表示されます。
  
**ADRPARM** 構造体の **ulFlags** メンバーの最も重要な 4 ビットには、ADRPARM 構造のバージョンを識別する **バージョン番号が含** まれている。 現在のバージョンは 0 (ゼロ) または ADRPARM_HELP_CTX。 MAPI の現在の実装は、0 以外の任意のバージョンの構造体に対して失敗します。 
  
将来のバージョンの構造は完全に異なる場合があります。バージョン 0 の構造をサポートしていない場合があります。 **ulFlags** メンバーからバージョン番号を抽出し、それを定義されたフラグと組み合わせるには、次のマクロが用意されています。 
  
- **GET_ADRPARM_VERSION** (_ulFlags_) 
- **SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _) 
- **ADRPARM_HELP_CTX**
  
## <a name="see-also"></a>関連項目

- [ACCELERATEABSDI](accelerateabsdi.md)
- [DISMISSMODELESS](dismissmodeless.md)
- [IAddrBook::Address](iaddrbook-address.md)
- [IMAPISupport::Address](imapisupport-address.md)
- [SRestriction](srestriction.md)
- [MAPI の構造](mapi-structures.md)

