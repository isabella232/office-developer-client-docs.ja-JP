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
ms.openlocfilehash: 9663a25a50d914f47cff48124898d16318bbbc43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330220"
---
# <a name="adrparm"></a><span data-ttu-id="912cf-103">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="912cf-103">ADRPARM</span></span>

<span data-ttu-id="912cf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="912cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="912cf-105">[共通アドレス] ダイアログボックスの表示と動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="912cf-105">Describes the display and behavior of the common address dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="912cf-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="912cf-106">Header file:</span></span>  <br/> |<span data-ttu-id="912cf-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="912cf-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="912cf-108">Members</span><span class="sxs-lookup"><span data-stu-id="912cf-108">Members</span></span>

<span data-ttu-id="912cf-109">**cbABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="912cf-109">**cbABContEntryID**</span></span>
  
> <span data-ttu-id="912cf-110">**lpabコンテ entryid**によって指摘されたエントリ識別子のバイト数。</span><span class="sxs-lookup"><span data-stu-id="912cf-110">Count of bytes in the entry identifier pointed to by **lpABContEntryID**.</span></span>
    
<span data-ttu-id="912cf-111">**lpabクレヨン entryid**</span><span class="sxs-lookup"><span data-stu-id="912cf-111">**lpABContEntryID**</span></span>
  
> <span data-ttu-id="912cf-112">[アドレス] ダイアログボックスに表示される受信者アドレスの初期のリストを提供するコンテナーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="912cf-112">Pointer to the entry identifier of the container that supplies the initial list of recipient addresses that are displayed in the address dialog box.</span></span>
    
<span data-ttu-id="912cf-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="912cf-113">**ulFlags**</span></span>
  
> <span data-ttu-id="912cf-114">さまざまな address ダイアログボックスオプションに関連付けられているフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="912cf-114">Bitmask of flags associated with various address dialog box options.</span></span> <span data-ttu-id="912cf-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="912cf-115">The following flags can be set:</span></span>
    
<span data-ttu-id="912cf-116">AB_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="912cf-116">AB_RESOLVE</span></span>
  
> <span data-ttu-id="912cf-117">[アドレス] ダイアログボックスを閉じた後、すべての名前を解決できるようにします。</span><span class="sxs-lookup"><span data-stu-id="912cf-117">Enable all names to be resolved after the address dialog box is closed.</span></span> <span data-ttu-id="912cf-118">名前解決プロセスの結果としてあいまいなエントリが表示された場合は、その解決のためにユーザーに確認するダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-118">If there are ambiguous entries that result from the name resolution process, a dialog box appears to prompt the user for help in resolving them.</span></span> <span data-ttu-id="912cf-119">このフラグを設定すると、 [IAddrBook:: アドレス](iaddrbook-address.md)で返されるすべての名前が解決されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-119">Setting this flag guarantees that all of the names returned by [IAddrBook::Address](iaddrbook-address.md) are resolved.</span></span> 
    
<span data-ttu-id="912cf-120">AB_SELECTONLY</span><span class="sxs-lookup"><span data-stu-id="912cf-120">AB_SELECTONLY</span></span>
  
> <span data-ttu-id="912cf-121">受信者リストの1回限りのアドレスの作成を無効にします。</span><span class="sxs-lookup"><span data-stu-id="912cf-121">Disable the creation of one-off addresses for a recipient list.</span></span> <span data-ttu-id="912cf-122">このフラグは、DIALOG_MODAL フラグが設定されている場合のように、ダイアログボックスがモーダルである場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-122">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span>
    
<span data-ttu-id="912cf-123">ADDRESS_ONE</span><span class="sxs-lookup"><span data-stu-id="912cf-123">ADDRESS_ONE</span></span>
  
> <span data-ttu-id="912cf-124">ユーザーは、リストから複数の受信者の代わりに1人の受信者を選択できます。</span><span class="sxs-lookup"><span data-stu-id="912cf-124">The user can select exactly one recipient instead of multiple recipients from a list.</span></span> <span data-ttu-id="912cf-125">このフラグは、 **cdestfields**が0で、ダイアログボックスがモーダルで、DIALOG_MODAL フラグが設定されている場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="912cf-125">This flag is valid only when **cDestFields** is zero and the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="912cf-126">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="912cf-126">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="912cf-127">[共通アドレス] ダイアログボックスのモーダルバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-127">Causes the modal version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="912cf-128">このフラグまたは DIALOG_SDI のいずれかを設定する必要があります。両方を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="912cf-128">Either this flag or DIALOG_SDI should be set; they cannot both be set.</span></span> 
    
<span data-ttu-id="912cf-129">DIALOG_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="912cf-129">DIALOG_OPTIONS</span></span>
  
> <span data-ttu-id="912cf-130">ダイアログボックスに [**送信オプション**] ボタンを表示します。</span><span class="sxs-lookup"><span data-stu-id="912cf-130">Causes the **Send Options** button to be displayed in the dialog box.</span></span> <span data-ttu-id="912cf-131">このフラグは、DIALOG_MODAL フラグが設定されている場合のように、ダイアログボックスがモーダルである場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-131">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="912cf-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="912cf-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="912cf-133">[共通アドレス] ダイアログボックスのモードレスバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-133">Causes the modeless version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="912cf-134">このフラグまたは DIALOG_MODAL のいずれかを設定する必要があります。両方を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="912cf-134">Either this flag or DIALOG_MODAL should be set; they cannot both be set.</span></span> <span data-ttu-id="912cf-135">Outlook 以外のクライアントでは、DIALOG_SDI フラグは無視され、ダイアログボックスのモーダルバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-135">The DIALOG_SDI flag is ignored for non-Outlook clients, and the modal version of the dialog box will be displayed.</span></span> <span data-ttu-id="912cf-136">そのため、 [IAddrBook:: Address](iaddrbook-address.md)の_lアウト uiparam_パラメーターでは、ハンドルへのポインターを想定しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="912cf-136">Consequently, a pointer to a handle should not be expected in the  _lpulUIParam_ parameter of [IAddrBook::Address](iaddrbook-address.md).</span></span>
    
<span data-ttu-id="912cf-137">**lpreserved**</span><span class="sxs-lookup"><span data-stu-id="912cf-137">**lpReserved**</span></span>
  
> <span data-ttu-id="912cf-138">予約済み。0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="912cf-138">Reserved, must be zero.</span></span>
    
<span data-ttu-id="912cf-139">**ulhelpcontext**</span><span class="sxs-lookup"><span data-stu-id="912cf-139">**ulHelpContext**</span></span>
  
> <span data-ttu-id="912cf-140">ユーザーが [アドレス] ダイアログボックスの [ヘルプ] ボタンをクリックしたときに最初に表示される**ヘルプ**内のコンテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="912cf-140">Specifies the context within **Help** that will first be shown when the user clicks the Help button in the address dialog box.</span></span> 
    
<span data-ttu-id="912cf-141">**lpszhelpfilename**</span><span class="sxs-lookup"><span data-stu-id="912cf-141">**lpszHelpFileName**</span></span>
  
> <span data-ttu-id="912cf-142">[アドレス] ダイアログボックスに関連付けられたヘルプファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="912cf-142">Pointer to the name of a Help file that will be associated with the address dialog box.</span></span> <span data-ttu-id="912cf-143">**lpszhelpfilename**メンバーは、Windows **WinHelp**関数を呼び出すために**ulhelpcontext**と共に使用されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-143">The **lpszHelpFileName** member is used together with **ulHelpContext** to call the Windows **WinHelp** function.</span></span> 
    
<span data-ttu-id="912cf-144">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="912cf-144">**lpfnABSDI**</span></span>
  
> <span data-ttu-id="912cf-145">[ACCELERATEABSDI](accelerateabsdi.md) prototype または NULL に基づく MAPI 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="912cf-145">Pointer to a MAPI function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype or NULL.</span></span> <span data-ttu-id="912cf-146">このメンバーは、DIALOG_SDI フラグが設定されている場合にのみ、ダイアログボックスのモードレスバージョンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-146">This member applies to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="912cf-147">[IAddrBook:: Address](iaddrbook-address.md)に渡す**ADRPARM**構造を構築しているクライアントは、常に**lpfnABSDI**メンバーを NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="912cf-147">Clients building an **ADRPARM** structure to pass to [IAddrBook::Address](iaddrbook-address.md) must always set the **lpfnABSDI** member to NULL.</span></span> <span data-ttu-id="912cf-148">DIALOG_SDI フラグが設定されている場合、MAPI は返される前に有効な関数に設定します。</span><span class="sxs-lookup"><span data-stu-id="912cf-148">If the DIALOG_SDI flag is set, MAPI will then set it to a valid function before returning.</span></span> <span data-ttu-id="912cf-149">クライアントは、メッセージループでこの関数を呼び出して、[アドレス帳] ダイアログボックスのアクセラレータが機能することを確認します。</span><span class="sxs-lookup"><span data-stu-id="912cf-149">Clients call this function from in their message loop to make sure that accelerators in the address book dialog box work.</span></span> <span data-ttu-id="912cf-150">ダイアログボックスが閉じられ、MAPI が**lpfnDismiss**メンバーによって示される関数を呼び出すと、クライアントは、メッセージループから**ACCELERATEABSDI**関数をアンフックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="912cf-150">When the dialog box is dismissed and MAPI calls the function pointed to by the **lpfnDismiss** member, clients should unhook the **ACCELERATEABSDI** function from their message loop.</span></span> 
    
<span data-ttu-id="912cf-151">**lpfnDismiss**</span><span class="sxs-lookup"><span data-stu-id="912cf-151">**lpfnDismiss**</span></span>
  
> <span data-ttu-id="912cf-152">[DISMISSMODELESS](dismissmodeless.md) prototype または NULL に基づく関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="912cf-152">Pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype or NULL.</span></span> <span data-ttu-id="912cf-153">このメンバーは、DIALOG_SDI フラグが設定されている場合にのみ、ダイアログボックスのモードレスバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-153">This member applies only to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="912cf-154">ユーザーが [モードレスアドレス] ダイアログボックスを閉じたときに MAPI が**DISMISSMODELESS**関数を呼び出し、 **IAddrBook::** を呼び出していることをクライアントに通知します。このダイアログボックスはアクティブではなくなっています。</span><span class="sxs-lookup"><span data-stu-id="912cf-154">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active.</span></span> 
    
<span data-ttu-id="912cf-155">**lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="912cf-155">**lpvDismissContext**</span></span>
  
> <span data-ttu-id="912cf-156">**lpfnDismiss**メンバーが指す**DISMISSMODELESS**関数に渡されるコンテキスト情報へのポインター。</span><span class="sxs-lookup"><span data-stu-id="912cf-156">Pointer to context information to be passed to the **DISMISSMODELESS** function pointed to by the **lpfnDismiss** member.</span></span> <span data-ttu-id="912cf-157">このメンバーは、DIALOG_SDI フラグが設定されている場合のように、ダイアログボックスのモードレスバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-157">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> 
    
<span data-ttu-id="912cf-158">**lpszcaption**</span><span class="sxs-lookup"><span data-stu-id="912cf-158">**lpszCaption**</span></span>
  
> <span data-ttu-id="912cf-159">[共通アドレス] ダイアログボックスのタイトルとして使用するテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="912cf-159">Pointer to text to be used as the title for the common address dialog box.</span></span>
    
<span data-ttu-id="912cf-160">**lpsznewentrytitle**</span><span class="sxs-lookup"><span data-stu-id="912cf-160">**lpszNewEntryTitle**</span></span>
  
> <span data-ttu-id="912cf-161">[**新しいエントリ**] ダイアログボックスまたは別のダイアログボックスを起動するボタンのボタンラベルとして使用するテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="912cf-161">Pointer to text to be used as the button label for the button that invokes either the **New Entry** dialog box or another dialog box.</span></span> 
    
<span data-ttu-id="912cf-162">**lpszDestWellsTitle**</span><span class="sxs-lookup"><span data-stu-id="912cf-162">**lpszDestWellsTitle**</span></span>
  
> <span data-ttu-id="912cf-163">[宛先] テキストボックスコントロールのタイトルとして使用するテキストへのポインターです。これは、[共通アドレス] ダイアログボックスのモーダルバージョンに表示されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-163">Pointer to text to be used as a title for the recipient text box controls that can appear in the modal version of the common address dialog box.</span></span> <span data-ttu-id="912cf-164">このメンバーは、モードレスダイアログボックスでは使用されません。</span><span class="sxs-lookup"><span data-stu-id="912cf-164">This member is not used for modeless dialog boxes.</span></span> 
    
<span data-ttu-id="912cf-165">**cdestfields**</span><span class="sxs-lookup"><span data-stu-id="912cf-165">**cDestFields**</span></span>
  
> <span data-ttu-id="912cf-166">[アドレス] ダイアログボックスのモーダルバージョンに含まれる受信者テキストボックスコントロールの数、またはダイアログボックスがモードレスの場合は0になります。</span><span class="sxs-lookup"><span data-stu-id="912cf-166">Count of recipient text box controls in the modal version of the address dialog box, or zero if the dialog box is modeless.</span></span> <span data-ttu-id="912cf-167">[アドレス] ダイアログボックスは、次の条件が満たされている場合にのみブラウズ用に開かれます。</span><span class="sxs-lookup"><span data-stu-id="912cf-167">The address dialog box is open for browsing only when the following conditions are true:</span></span> 
    
  - <span data-ttu-id="912cf-168">**cdestfields**メンバーが0に設定されています。</span><span class="sxs-lookup"><span data-stu-id="912cf-168">The **cDestFields** member is set to zero.</span></span> 
    
  - <span data-ttu-id="912cf-169">DIALOG_BOX フラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="912cf-169">The DIALOG_BOX flag is set.</span></span>
    
  - <span data-ttu-id="912cf-170">ADDRESS_ONE フラグが設定されていません。</span><span class="sxs-lookup"><span data-stu-id="912cf-170">The ADDRESS_ONE flag is not set.</span></span>
    
  <span data-ttu-id="912cf-171">**cdestfields**を0xffffffff に設定すると、MAPI は受信者テキストボックスコントロールの既定の数を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="912cf-171">Setting **cDestFields** to 0XFFFFFFFF implies that MAPI should create the default number of recipient text box controls.</span></span> <span data-ttu-id="912cf-172">この場合、 **lppszdesttitles**メンバーおよび**lアウト destカンプ**メンバーは NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="912cf-172">In this case, the **lppszDestTitles** and **lpulDestComps** members must be NULL.</span></span> 
    
<span data-ttu-id="912cf-173">**ndestfieldfocus**</span><span class="sxs-lookup"><span data-stu-id="912cf-173">**nDestFieldFocus**</span></span>
  
> <span data-ttu-id="912cf-174">モーダルバージョンのダイアログボックスが表示されるときに最初にフォーカスする必要があるテキストボックスコントロールを示します。</span><span class="sxs-lookup"><span data-stu-id="912cf-174">Indicates the particular text box control that should have the initial focus when the modal version of the dialog box appears.</span></span> <span data-ttu-id="912cf-175">この値は、0から**cdestfields**から1を引いた値までの範囲にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="912cf-175">This value must be between 0 and the value of **cDestFields** minus 1.</span></span> 
    
<span data-ttu-id="912cf-176">**lppszdesttitles**</span><span class="sxs-lookup"><span data-stu-id="912cf-176">**lppszDestTitles**</span></span>
  
> <span data-ttu-id="912cf-177">[アドレス] ダイアログボックスのモーダルバージョンに表示される各テキストボックスコントロールに関連付けられているボタンのラベルの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="912cf-177">Pointer to an array of labels for buttons associated with each of the text box controls that are displayed in the modal version of the address dialog box.</span></span> <span data-ttu-id="912cf-178">**cdestfields**メンバーの値は、配列に含まれているラベルの数を示します。</span><span class="sxs-lookup"><span data-stu-id="912cf-178">The value of the **cDestFields** member indicates the number of labels included in the array.</span></span> <span data-ttu-id="912cf-179">**lppszdesttitles**メンバーが NULL の場合、 **Address**メソッドは既定のタイトルを使用します。</span><span class="sxs-lookup"><span data-stu-id="912cf-179">If the **lppszDestTitles** member is NULL, the **Address** method uses default titles.</span></span> 
    
<span data-ttu-id="912cf-180">**lアウト destカンプ**</span><span class="sxs-lookup"><span data-stu-id="912cf-180">**lpulDestComps**</span></span>
  
> <span data-ttu-id="912cf-181">各テキストボックスコントロールに関連付けられている、MAPI_TO、MAPI_CC、MAPI_BCC などの受信者の種類の値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="912cf-181">Pointer to an array of recipient type values, such as MAPI_TO, MAPI_CC, and MAPI_BCC, that is associated with each text box control.</span></span> <span data-ttu-id="912cf-182">**cdestfields**メンバーの値は、配列に含まれる受信者の種類の数を示します。</span><span class="sxs-lookup"><span data-stu-id="912cf-182">The value of the **CDestFields** member indicates the number of recipient types included in the array.</span></span> <span data-ttu-id="912cf-183">**lPR_RECIPIENT_TYPE destカンプ**が指す値を使用して、各受信者の\*\*\*\* ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="912cf-183">The values pointed to by **lpulDestComps** can be used to set the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property of each recipient.</span></span> <span data-ttu-id="912cf-184">**lpuldestcomps**メンバーが NULL の場合、 **Address**メソッドは既定の受信者の種類を使用します。</span><span class="sxs-lookup"><span data-stu-id="912cf-184">If the **lpulDestComps** member is NULL, the **Address** method uses default recipient types.</span></span> 
    
<span data-ttu-id="912cf-185">**lpコンテ制限**</span><span class="sxs-lookup"><span data-stu-id="912cf-185">**lpContRestriction**</span></span>
  
> <span data-ttu-id="912cf-186">ダイアログボックスに表示できるアドレスエントリの種類を制限する[srestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="912cf-186">Pointer to an [SRestriction](srestriction.md) structure that limits the type of address entries that can be displayed in the dialog box.</span></span> 
    
<span data-ttu-id="912cf-187">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="912cf-187">**lpHierRestriction**</span></span>
  
> <span data-ttu-id="912cf-188">ダイアログボックスに表示されるアドレスエントリを提供できるアドレス帳のコンテナーを制限する**srestriction**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="912cf-188">Pointer to an **SRestriction** structure that limits the address book containers that can supply address entries to be displayed in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="912cf-189">解説</span><span class="sxs-lookup"><span data-stu-id="912cf-189">Remarks</span></span>

<span data-ttu-id="912cf-190">**ADRPARM**構造体は、クライアントとサービスプロバイダーによって、MAPI の共通アドレスダイアログボックスの外観と動作を制御するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-190">**ADRPARM** structures are used by clients and service providers to control the appearance and behavior of the MAPI common address dialog boxes.</span></span> <span data-ttu-id="912cf-191">[アドレス] ダイアログボックスには、モードレスとモーダルの2種類があります。</span><span class="sxs-lookup"><span data-stu-id="912cf-191">There are two varieties of the address dialog box: modeless and modal.</span></span> <span data-ttu-id="912cf-192">**ADRPARM**構造体のメンバーの中には、ダイアログボックスの両方のバージョンに適用されるものもありますが、一部は2つのバージョンのどちらかにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-192">Some of the members in the **ADRPARM** structure apply to both versions of the dialog box, but some only apply to one of the two versions.</span></span> <span data-ttu-id="912cf-193">次の表では、 **ADRPARM**構造体のメンバーを、共通のアドレスダイアログボックスで使用する方法に関連しています。</span><span class="sxs-lookup"><span data-stu-id="912cf-193">The following table relates the members of an **ADRPARM** structure to their use with the common address dialog boxes.</span></span> 
  
|<span data-ttu-id="912cf-194">ADRPARM メンバー</span><span class="sxs-lookup"><span data-stu-id="912cf-194">ADRPARM member</span></span>|<span data-ttu-id="912cf-195">ダイアログボックスの種類</span><span class="sxs-lookup"><span data-stu-id="912cf-195">Type of dialog box</span></span>|
|:-----|:-----|
|<span data-ttu-id="912cf-196">**cbABContEntryID**および**lpabクレヨン entryid**</span><span class="sxs-lookup"><span data-stu-id="912cf-196">**cbABContEntryID** and **lpABContEntryID**</span></span> <br/> |<span data-ttu-id="912cf-197">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="912cf-197">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="912cf-198">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="912cf-198">**ulFlags**</span></span> <br/> |<span data-ttu-id="912cf-199">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="912cf-199">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="912cf-200">**lpreserved**</span><span class="sxs-lookup"><span data-stu-id="912cf-200">**lpReserved**</span></span> <br/> |<span data-ttu-id="912cf-201">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="912cf-201">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="912cf-202">**ulhelpcontext**と**lpszhelpfilename**</span><span class="sxs-lookup"><span data-stu-id="912cf-202">**ulHelpContext** and **lpszHelpFileName**</span></span> <br/> |<span data-ttu-id="912cf-203">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="912cf-203">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="912cf-204">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="912cf-204">**lpfnABSDI**</span></span> <br/> |<span data-ttu-id="912cf-205">Modeless</span><span class="sxs-lookup"><span data-stu-id="912cf-205">Modeless</span></span>  <br/> |
|<span data-ttu-id="912cf-206">**lpfnDismiss**および**lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="912cf-206">**lpfnDismiss** and **lpvDismissContext**</span></span> <br/> |<span data-ttu-id="912cf-207">Modeless</span><span class="sxs-lookup"><span data-stu-id="912cf-207">Modeless</span></span>  <br/> |
|<span data-ttu-id="912cf-208">**lpszcaption**</span><span class="sxs-lookup"><span data-stu-id="912cf-208">**lpszCaption**</span></span> <br/> |<span data-ttu-id="912cf-209">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="912cf-209">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="912cf-210">**lpsznewentrytitle**</span><span class="sxs-lookup"><span data-stu-id="912cf-210">**lpszNewEntryTitle**</span></span> <br/> |<span data-ttu-id="912cf-211">Modal</span><span class="sxs-lookup"><span data-stu-id="912cf-211">Modal</span></span>  <br/> |
|<span data-ttu-id="912cf-212">**lpszDestWellsTitle**、 **cdestfields**、 **ndestfieldfocus**、 **lppszdesttitles**、 **lindexdestカンプ**</span><span class="sxs-lookup"><span data-stu-id="912cf-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**, and **lpulDestComps**</span></span> <br/> |<span data-ttu-id="912cf-213">Modal</span><span class="sxs-lookup"><span data-stu-id="912cf-213">Modal</span></span>  <br/> |
|<span data-ttu-id="912cf-214">**lpコンテ制限**</span><span class="sxs-lookup"><span data-stu-id="912cf-214">**lpContRestriction**</span></span> <br/> |<span data-ttu-id="912cf-215">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="912cf-215">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="912cf-216">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="912cf-216">**lpHierRestriction**</span></span> <br/> |<span data-ttu-id="912cf-217">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="912cf-217">Modal and modeless</span></span>  <br/> |
   
<span data-ttu-id="912cf-218">モードレスダイアログボックスは、1つまたは複数のアドレス帳コンテナーからのエントリを読み取り専用で表示します。</span><span class="sxs-lookup"><span data-stu-id="912cf-218">The modeless dialog box is a read-only display of entries from one or more address book containers.</span></span> <span data-ttu-id="912cf-219">このダイアログボックスでは、選択したコンテナーからのすべてのエントリを表示することも、制限によって設定された条件に一致するエントリとコンテナーのみに制限することもできます。</span><span class="sxs-lookup"><span data-stu-id="912cf-219">The dialog box can display all entries from the selected containers or be limited to only those entries and containers that match criteria established by a restriction.</span></span> <span data-ttu-id="912cf-220">**lpコンテ制限**によって参照されるコンテンツ制限によって、表示されるエントリの種類と、 **lpHierRestriction**によって示される階層制限によって、エントリを提供するコンテナーを制限できます。</span><span class="sxs-lookup"><span data-stu-id="912cf-220">The contents restriction pointed to by **lpContRestriction** can limit the types of entries displayed and the hierarchy restriction pointed to by **lpHierRestriction** can limit the containers providing the entries.</span></span> <span data-ttu-id="912cf-221">ダイアログボックスが閉じられたときに発信者に通知するために、MAPI は、 [DISMISSMODELESS](dismissmodeless.md)プロトタイプに一致する呼び出し元によって提供される関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="912cf-221">To inform the caller when the dialog box is dismissed, MAPI invokes a function that is provided by the caller that matches the [DISMISSMODELESS](dismissmodeless.md) prototype.</span></span> <span data-ttu-id="912cf-222">[ACCELERATEABSDI](accelerateabsdi.md)プロトタイプに一致するもう1つの関数は MAPI によって提供され、Windows メッセージループで呼び出し元によって呼び出され、キーボードショートカットの動作を容易にします。</span><span class="sxs-lookup"><span data-stu-id="912cf-222">Another function, one that matches the [ACCELERATEABSDI](accelerateabsdi.md) prototype, is provided by MAPI and invoked by the caller in the Windows message loop to facilitate the working of keyboard shortcuts.</span></span> <span data-ttu-id="912cf-223">クライアントが[IAddrBook:: アドレス](iaddrbook-address.md)を呼び出したとき、またはサービスプロバイダーが[imapisupport:: address](imapisupport-address.md)を呼び出したときに、モードレスバージョンの [MAPI アドレス] ダイアログボックスが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="912cf-223">The modeless version of the MAPI address dialog box can be displayed when clients call [IAddrBook::Address](iaddrbook-address.md) or when service providers call [IMAPISupport::Address](imapisupport-address.md).</span></span> 
  
<span data-ttu-id="912cf-224">モーダルダイアログボックスは、1つまたは複数のコンテナーからのエントリを読み取り/書き込みで表示します。</span><span class="sxs-lookup"><span data-stu-id="912cf-224">The modal dialog box is a read/write display of entries from one or more containers.</span></span> <span data-ttu-id="912cf-225">この内容は、 **lpコンテ制限**および**lpHierRestriction**メンバーで設定された制限によって、モードレスバージョンと同じ方法で影響を受ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="912cf-225">Its contents can be affected in the same manner as the modeless version by restrictions set in the **lpContRestriction** and **lpHierRestriction** members.</span></span> <span data-ttu-id="912cf-226">コンテナーエントリを表示するリストボックスに加えて、モーダルダイアログボックスには、ユーザーによって選択されたエントリを保持するためのテキストボックスコントロールを 1 ~ 3 個まで含めることができます。</span><span class="sxs-lookup"><span data-stu-id="912cf-226">In addition to the list box displaying container entries, the modal dialog box can contain between one and three text box controls for holding entries selected by the user.</span></span> <span data-ttu-id="912cf-227">各編集コントロールは、MAPI_TO などの特定の受信者の種類または**PR_RECIPIENT_TYPE**プロパティに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="912cf-227">Each edit control is associated with a particular recipient type or **PR_RECIPIENT_TYPE** property such as MAPI_TO.</span></span> <span data-ttu-id="912cf-228">[モーダルアドレス] ダイアログボックスを表示するには、いずれかの**アドレス**方法を使用するか、クライアントが[IAddrBook](iaddrbook-details.md)を呼び出すときに、etails とサービスプロバイダーの呼び出し[imapisupport::D etails](imapisupport-details.md)を使用します。</span><span class="sxs-lookup"><span data-stu-id="912cf-228">The modal address dialog box can be displayed by either of the **Address** methods or when clients call [IAddrBook::Details](iaddrbook-details.md) and service providers call [IMAPISupport::Details](imapisupport-details.md).</span></span> 
  
<span data-ttu-id="912cf-229">この図には2つのテキストボックスコントロールが含まれています。このダイアログボックスの表示を制御する**ADRPARM**構造体の**cdestfields**メンバーは2に設定されています。</span><span class="sxs-lookup"><span data-stu-id="912cf-229">This illustration includes two text box controls because the **cDestFields** member of the **ADRPARM** structure controlling the display of this dialog box is set to 2.</span></span> <span data-ttu-id="912cf-230">**ndestfieldfocus**メンバーが0に設定されているため、最初のコントロールには最初のフォーカスがあります。</span><span class="sxs-lookup"><span data-stu-id="912cf-230">The first control has initial focus because the **nDestFieldFocus** member is set to 0.</span></span> 
  
<span data-ttu-id="912cf-231">**lpsznewentrytitle**メンバーは、選択時にボタンラベルのテキストをポイントすると、追加のダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-231">The **lpszNewEntryTitle** member points to text for a button label that, when it is selected, causes an additional dialog box to be displayed.</span></span> <span data-ttu-id="912cf-232">通常、モーダルダイアログボックスの図に示されているように、ボタンに [**新規**] というラベルが付けられ、表示されるダイアログボックスに、プロファイル内の任意のアドレス帳プロバイダーで作成できるアドレスの種類が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-232">Typically, as is shown in the illustration of the modal dialog box, the button is labeled **New** and the dialog box that appears lists all of the types of addresses that can be created by any of the address book providers in the profile.</span></span> <span data-ttu-id="912cf-233">クライアントは[IAddrBook:: newentry](iaddrbook-newentry.md)を呼び出し、 _cbeidnewentrytpl_パラメーターに0を渡し、ユーザーがボタンを選択したときに_lpeidnewentrytpl_パラメーターに NULL を渡すことによって、この**新しいエントリ**のダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-233">Clients cause this **New Entry** dialog box to be displayed by calling [IAddrBook::NewEntry](iaddrbook-newentry.md) and passing zero for the  _cbEidNewEntryTpl_ parameter and NULL for the  _lpEidNewEntryTpl_ parameter when the user selects the button.</span></span> <span data-ttu-id="912cf-234">このダイアログボックスに含まれる情報は、MAPI の1回限りのテーブルから取得されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-234">The information that is included in this dialog box comes from the MAPI one-off table.</span></span> 
  
<span data-ttu-id="912cf-235">このダイアログボックスのすべてのエントリは、特定の種類のアドレスを作成するために必要なデータを入力するためのテンプレートに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="912cf-235">Every entry in this dialog box is associated with a template for entering the data required to create an address of the particular type.</span></span> <span data-ttu-id="912cf-236">ほとんどのアドレス帳プロバイダーは、作成できるアドレスエントリの種類ごとに1つのテンプレートを提供します。</span><span class="sxs-lookup"><span data-stu-id="912cf-236">Most address book providers supply one template for every type of address entry they can create.</span></span> <span data-ttu-id="912cf-237">このダイアログボックスからユーザーが選択を行うと、MAPI には対応するテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="912cf-237">When a user makes a selection from this dialog box, MAPI displays the corresponding template.</span></span>
  
<span data-ttu-id="912cf-238">**ADRPARM**構造体の**ulflags**メンバーの最上位4ビットには、 **ADRPARM**構造のバージョンを識別するバージョン番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="912cf-238">The most significant four bits of the **ADRPARM** structure's **ulFlags** member contain a version number identifying the version of the **ADRPARM** structure.</span></span> <span data-ttu-id="912cf-239">現在のバージョンは 0 (ゼロ) または ADRPARM_HELP_CTX です。</span><span class="sxs-lookup"><span data-stu-id="912cf-239">The current version is 0 (zero) or ADRPARM_HELP_CTX.</span></span> <span data-ttu-id="912cf-240">現在の MAPI の実装は、ゼロ以外の構造体のバージョンでは失敗します。</span><span class="sxs-lookup"><span data-stu-id="912cf-240">The current implementation of MAPI will fail for any version of the structure other than zero.</span></span> 
  
<span data-ttu-id="912cf-241">将来の構造のバージョンは、まったく異なる場合があります。これらは、バージョン0の構造をサポートしていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="912cf-241">Future versions of the structure may be completely different; they may not support the version-zero structure.</span></span> <span data-ttu-id="912cf-242">**ulflags**メンバーからバージョン番号を抽出し、定義されたフラグと組み合わせるために、次のマクロが提供されています。</span><span class="sxs-lookup"><span data-stu-id="912cf-242">The following macros are provided for extracting the version number from the **ulFlags** member and for combining it with the defined flags:</span></span> 
  
- <span data-ttu-id="912cf-243">**GET_ADRPARM_VERSION**(_ulflags_)</span><span class="sxs-lookup"><span data-stu-id="912cf-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span></span> 
- <span data-ttu-id="912cf-244">**SET_ADRPARM_VERSION**(_ulflags_、_ ulflags _)</span><span class="sxs-lookup"><span data-stu-id="912cf-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span></span> 
- <span data-ttu-id="912cf-245">**ADRPARM_HELP_CTX**</span><span class="sxs-lookup"><span data-stu-id="912cf-245">**ADRPARM_HELP_CTX**</span></span>
  
## <a name="see-also"></a><span data-ttu-id="912cf-246">関連項目</span><span class="sxs-lookup"><span data-stu-id="912cf-246">See also</span></span>

- [<span data-ttu-id="912cf-247">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="912cf-247">ACCELERATEABSDI</span></span>](accelerateabsdi.md)
- [<span data-ttu-id="912cf-248">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="912cf-248">DISMISSMODELESS</span></span>](dismissmodeless.md)
- [<span data-ttu-id="912cf-249">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="912cf-249">IAddrBook::Address</span></span>](iaddrbook-address.md)
- [<span data-ttu-id="912cf-250">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="912cf-250">IMAPISupport::Address</span></span>](imapisupport-address.md)
- [<span data-ttu-id="912cf-251">SRestriction</span><span class="sxs-lookup"><span data-stu-id="912cf-251">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="912cf-252">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="912cf-252">MAPI Structures</span></span>](mapi-structures.md)

