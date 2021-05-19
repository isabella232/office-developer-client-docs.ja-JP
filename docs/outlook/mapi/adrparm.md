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
# <a name="adrparm"></a><span data-ttu-id="be0b5-103">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="be0b5-103">ADRPARM</span></span>

<span data-ttu-id="be0b5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be0b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be0b5-105">[共通アドレス] ダイアログ ボックスの表示と動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-105">Describes the display and behavior of the common address dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be0b5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="be0b5-106">Header file:</span></span>  <br/> |<span data-ttu-id="be0b5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="be0b5-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="be0b5-108">Members</span><span class="sxs-lookup"><span data-stu-id="be0b5-108">Members</span></span>

<span data-ttu-id="be0b5-109">**cbABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="be0b5-109">**cbABContEntryID**</span></span>
  
> <span data-ttu-id="be0b5-110">**lpABContEntryID** が指すエントリ識別子内のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="be0b5-110">Count of bytes in the entry identifier pointed to by **lpABContEntryID**.</span></span>
    
<span data-ttu-id="be0b5-111">**lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="be0b5-111">**lpABContEntryID**</span></span>
  
> <span data-ttu-id="be0b5-112">[アドレス] ダイアログ ボックスに表示される受信者アドレスの最初の一覧を提供するコンテナーのエントリ識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-112">Pointer to the entry identifier of the container that supplies the initial list of recipient addresses that are displayed in the address dialog box.</span></span>
    
<span data-ttu-id="be0b5-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="be0b5-113">**ulFlags**</span></span>
  
> <span data-ttu-id="be0b5-114">さまざまなアドレス ダイアログ ボックスオプションに関連付けられたフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="be0b5-114">Bitmask of flags associated with various address dialog box options.</span></span> <span data-ttu-id="be0b5-115">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-115">The following flags can be set:</span></span>
    
<span data-ttu-id="be0b5-116">AB_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="be0b5-116">AB_RESOLVE</span></span>
  
> <span data-ttu-id="be0b5-117">[アドレス] ダイアログ ボックスを閉じた後で、すべての名前を解決できます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-117">Enable all names to be resolved after the address dialog box is closed.</span></span> <span data-ttu-id="be0b5-118">名前解決プロセスの結果としてあいまいなエントリがある場合は、ユーザーに解決の助けを求めるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-118">If there are ambiguous entries that result from the name resolution process, a dialog box appears to prompt the user for help in resolving them.</span></span> <span data-ttu-id="be0b5-119">このフラグを設定すると [、IAddrBook::Address](iaddrbook-address.md) によって返される名前はすべて解決されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-119">Setting this flag guarantees that all of the names returned by [IAddrBook::Address](iaddrbook-address.md) are resolved.</span></span> 
    
<span data-ttu-id="be0b5-120">AB_SELECTONLY</span><span class="sxs-lookup"><span data-stu-id="be0b5-120">AB_SELECTONLY</span></span>
  
> <span data-ttu-id="be0b5-121">受信者リストの一時アドレスの作成を無効にします。</span><span class="sxs-lookup"><span data-stu-id="be0b5-121">Disable the creation of one-off addresses for a recipient list.</span></span> <span data-ttu-id="be0b5-122">このフラグは、ダイアログ ボックスがモーダルである場合にのみ使用されます。設定されているフラグDIALOG_MODAL示します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-122">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span>
    
<span data-ttu-id="be0b5-123">ADDRESS_ONE</span><span class="sxs-lookup"><span data-stu-id="be0b5-123">ADDRESS_ONE</span></span>
  
> <span data-ttu-id="be0b5-124">ユーザーは、リストから複数の受信者ではなく、正確に 1 つの受信者を選択できます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-124">The user can select exactly one recipient instead of multiple recipients from a list.</span></span> <span data-ttu-id="be0b5-125">このフラグは **、cDestFields** が 0 で、ダイアログ ボックスがモーダルである場合にのみ有効です。設定されているフラグDIALOG_MODAL示されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-125">This flag is valid only when **cDestFields** is zero and the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="be0b5-126">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="be0b5-126">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="be0b5-127">共通アドレス ダイアログ ボックスのモーダル バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-127">Causes the modal version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="be0b5-128">このフラグまたは設定DIALOG_SDI設定する必要があります。両方を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="be0b5-128">Either this flag or DIALOG_SDI should be set; they cannot both be set.</span></span> 
    
<span data-ttu-id="be0b5-129">DIALOG_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="be0b5-129">DIALOG_OPTIONS</span></span>
  
> <span data-ttu-id="be0b5-130">ダイアログ ボックスに **[オプション** の送信] ボタンを表示します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-130">Causes the **Send Options** button to be displayed in the dialog box.</span></span> <span data-ttu-id="be0b5-131">このフラグは、ダイアログ ボックスがモーダルである場合にのみ使用されます。設定されているフラグDIALOG_MODAL示します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-131">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="be0b5-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="be0b5-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="be0b5-133">[共通アドレス] ダイアログ ボックスのモードレス バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-133">Causes the modeless version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="be0b5-134">このフラグまたは設定DIALOG_MODAL設定する必要があります。両方を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="be0b5-134">Either this flag or DIALOG_MODAL should be set; they cannot both be set.</span></span> <span data-ttu-id="be0b5-135">クライアントDIALOG_SDIの Outlook場合、DIALOG_SDIフラグは無視され、ダイアログ ボックスのモーダル バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-135">The DIALOG_SDI flag is ignored for non-Outlook clients, and the modal version of the dialog box will be displayed.</span></span> <span data-ttu-id="be0b5-136">したがって [、IAddrBook::Address](iaddrbook-address.md)の _lpulUIParam_ パラメーターでは、ハンドルへのポインターを予期しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-136">Consequently, a pointer to a handle should not be expected in the  _lpulUIParam_ parameter of [IAddrBook::Address](iaddrbook-address.md).</span></span>
    
<span data-ttu-id="be0b5-137">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="be0b5-137">**lpReserved**</span></span>
  
> <span data-ttu-id="be0b5-138">予約済みで、ゼロである必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-138">Reserved, must be zero.</span></span>
    
<span data-ttu-id="be0b5-139">**ulHelpContext**</span><span class="sxs-lookup"><span data-stu-id="be0b5-139">**ulHelpContext**</span></span>
  
> <span data-ttu-id="be0b5-140">ユーザーが [アドレス **]** ダイアログ ボックスの [ヘルプ] ボタンをクリックすると最初に表示されるヘルプ内のコンテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-140">Specifies the context within **Help** that will first be shown when the user clicks the Help button in the address dialog box.</span></span> 
    
<span data-ttu-id="be0b5-141">**lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="be0b5-141">**lpszHelpFileName**</span></span>
  
> <span data-ttu-id="be0b5-142">アドレス ダイアログ ボックスに関連付けられるヘルプ ファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-142">Pointer to the name of a Help file that will be associated with the address dialog box.</span></span> <span data-ttu-id="be0b5-143">**lpszHelpFileName** メンバーは **、ulHelpContext** と共に使用して、winHelp 関数Windows **呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-143">The **lpszHelpFileName** member is used together with **ulHelpContext** to call the Windows **WinHelp** function.</span></span> 
    
<span data-ttu-id="be0b5-144">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="be0b5-144">**lpfnABSDI**</span></span>
  
> <span data-ttu-id="be0b5-145">[ACCELERATEABSDI](accelerateabsdi.md)プロトタイプまたは NULL に基づく MAPI 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-145">Pointer to a MAPI function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype or NULL.</span></span> <span data-ttu-id="be0b5-146">このメンバーは、設定されているオプション フラグで示されているモードレス DIALOG_SDIダイアログ ボックスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-146">This member applies to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="be0b5-147">[IAddrBook::Address](iaddrbook-address.md)に渡す **ADRPARM** 構造を構築するクライアントは、常に **lpfnABSDI** メンバーを NULL に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-147">Clients building an **ADRPARM** structure to pass to [IAddrBook::Address](iaddrbook-address.md) must always set the **lpfnABSDI** member to NULL.</span></span> <span data-ttu-id="be0b5-148">このフラグDIALOG_SDI設定すると、MAPI は返す前に有効な関数に設定されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-148">If the DIALOG_SDI flag is set, MAPI will then set it to a valid function before returning.</span></span> <span data-ttu-id="be0b5-149">クライアントは、メッセージ ループからこの関数を呼び出して、アドレス帳ダイアログ ボックスのアクセラレータが機能する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-149">Clients call this function from in their message loop to make sure that accelerators in the address book dialog box work.</span></span> <span data-ttu-id="be0b5-150">ダイアログ ボックスが閉じ、MAPI が **lpfnDismiss** メンバーが指す関数を呼び出す場合、クライアントはメッセージ ループから **ACCELERATEABSDI** 関数を解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-150">When the dialog box is dismissed and MAPI calls the function pointed to by the **lpfnDismiss** member, clients should unhook the **ACCELERATEABSDI** function from their message loop.</span></span> 
    
<span data-ttu-id="be0b5-151">**lpfnDismiss**</span><span class="sxs-lookup"><span data-stu-id="be0b5-151">**lpfnDismiss**</span></span>
  
> <span data-ttu-id="be0b5-152">[DISMISSMODELESS](dismissmodeless.md)プロトタイプまたは NULL に基づく関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-152">Pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype or NULL.</span></span> <span data-ttu-id="be0b5-153">このメンバーは、設定されているオプション フラグで示されているとおり、ダイアログ ボックスのモードレス バージョンにのみ適用されます。DIALOG_SDIします。</span><span class="sxs-lookup"><span data-stu-id="be0b5-153">This member applies only to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="be0b5-154">MAPI は、ユーザーがモードレス アドレス ダイアログ ボックスを閉じ、ダイアログ ボックスがアクティブでなくなった **IAddrBook::Address** を呼び出すクライアントに通知するときに **DISMISSMODELESS** 関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-154">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active.</span></span> 
    
<span data-ttu-id="be0b5-155">**lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="be0b5-155">**lpvDismissContext**</span></span>
  
> <span data-ttu-id="be0b5-156">**lpfnDismiss** メンバーが指す **DISMISSMODELESS** 関数に渡されるコンテキスト情報へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-156">Pointer to context information to be passed to the **DISMISSMODELESS** function pointed to by the **lpfnDismiss** member.</span></span> <span data-ttu-id="be0b5-157">このメンバーは、設定されているオプション フラグで示されているモードレス DIALOG_SDIダイアログ ボックスにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-157">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> 
    
<span data-ttu-id="be0b5-158">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="be0b5-158">**lpszCaption**</span></span>
  
> <span data-ttu-id="be0b5-159">共通アドレス ダイアログ ボックスのタイトルとして使用するテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-159">Pointer to text to be used as the title for the common address dialog box.</span></span>
    
<span data-ttu-id="be0b5-160">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="be0b5-160">**lpszNewEntryTitle**</span></span>
  
> <span data-ttu-id="be0b5-161">[新しいエントリ] ダイアログ ボックスまたは別のダイアログ ボックスを呼び出すボタンのボタン ラベルとして使用するテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-161">Pointer to text to be used as the button label for the button that invokes either the **New Entry** dialog box or another dialog box.</span></span> 
    
<span data-ttu-id="be0b5-162">**lpszDestWellsTitle**</span><span class="sxs-lookup"><span data-stu-id="be0b5-162">**lpszDestWellsTitle**</span></span>
  
> <span data-ttu-id="be0b5-163">共通アドレス ダイアログ ボックスのモーダル バージョンに表示できる受信者テキスト ボックス コントロールのタイトルとして使用するテキストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-163">Pointer to text to be used as a title for the recipient text box controls that can appear in the modal version of the common address dialog box.</span></span> <span data-ttu-id="be0b5-164">このメンバーは、モードレス ダイアログ ボックスには使用されません。</span><span class="sxs-lookup"><span data-stu-id="be0b5-164">This member is not used for modeless dialog boxes.</span></span> 
    
<span data-ttu-id="be0b5-165">**cDestFields**</span><span class="sxs-lookup"><span data-stu-id="be0b5-165">**cDestFields**</span></span>
  
> <span data-ttu-id="be0b5-166">モーダル バージョンのアドレス ダイアログ ボックスの受信者テキスト ボックス コントロールの数、またはダイアログ ボックスがモードレスの場合は 0。</span><span class="sxs-lookup"><span data-stu-id="be0b5-166">Count of recipient text box controls in the modal version of the address dialog box, or zero if the dialog box is modeless.</span></span> <span data-ttu-id="be0b5-167">[アドレス] ダイアログ ボックスは、次の条件が満たされている場合にのみ参照用に開きます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-167">The address dialog box is open for browsing only when the following conditions are true:</span></span> 
    
  - <span data-ttu-id="be0b5-168">**cDestFields メンバーは** 0 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-168">The **cDestFields** member is set to zero.</span></span> 
    
  - <span data-ttu-id="be0b5-169">このDIALOG_BOXが設定されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-169">The DIALOG_BOX flag is set.</span></span>
    
  - <span data-ttu-id="be0b5-170">このADDRESS_ONEフラグは設定されていない。</span><span class="sxs-lookup"><span data-stu-id="be0b5-170">The ADDRESS_ONE flag is not set.</span></span>
    
  <span data-ttu-id="be0b5-171">**cDestFields を 0XFFFFFFFF** すると、MAPI は受信者テキスト ボックス コントロールの既定の数を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-171">Setting **cDestFields** to 0XFFFFFFFF implies that MAPI should create the default number of recipient text box controls.</span></span> <span data-ttu-id="be0b5-172">この場合 **、lppszDestTitles および** **lpulDestComps メンバー** は NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-172">In this case, the **lppszDestTitles** and **lpulDestComps** members must be NULL.</span></span> 
    
<span data-ttu-id="be0b5-173">**nDestFieldFocus**</span><span class="sxs-lookup"><span data-stu-id="be0b5-173">**nDestFieldFocus**</span></span>
  
> <span data-ttu-id="be0b5-174">ダイアログ ボックスのモーダル バージョンが表示される場合に、最初のフォーカスを持つ必要がある特定のテキスト ボックス コントロールを示します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-174">Indicates the particular text box control that should have the initial focus when the modal version of the dialog box appears.</span></span> <span data-ttu-id="be0b5-175">この値は、0 から **cDestFields** から 1 を引いた値の間である必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-175">This value must be between 0 and the value of **cDestFields** minus 1.</span></span> 
    
<span data-ttu-id="be0b5-176">**lppszDestTitles**</span><span class="sxs-lookup"><span data-stu-id="be0b5-176">**lppszDestTitles**</span></span>
  
> <span data-ttu-id="be0b5-177">モーダル バージョンのアドレス ダイアログ ボックスに表示される各テキスト ボックス コントロールに関連付けられたボタンのラベルの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-177">Pointer to an array of labels for buttons associated with each of the text box controls that are displayed in the modal version of the address dialog box.</span></span> <span data-ttu-id="be0b5-178">**cDestFields メンバーの値** は、配列に含まれるラベルの数を示します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-178">The value of the **cDestFields** member indicates the number of labels included in the array.</span></span> <span data-ttu-id="be0b5-179">**lppszDestTitles メンバー** が NULL の場合 **、Address** メソッドは既定のタイトルを使用します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-179">If the **lppszDestTitles** member is NULL, the **Address** method uses default titles.</span></span> 
    
<span data-ttu-id="be0b5-180">**lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="be0b5-180">**lpulDestComps**</span></span>
  
> <span data-ttu-id="be0b5-181">各テキスト ボックス コントロールに関連付けられている MAPI_TO、MAPI_CC、MAPI_BCC など、受信者の種類の値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-181">Pointer to an array of recipient type values, such as MAPI_TO, MAPI_CC, and MAPI_BCC, that is associated with each text box control.</span></span> <span data-ttu-id="be0b5-182">**CDestFields** メンバーの値は、配列に含まれる受信者の種類の数を示します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-182">The value of the **CDestFields** member indicates the number of recipient types included in the array.</span></span> <span data-ttu-id="be0b5-183">**lpulDestComps** が指す値を使用して、各受信者の PR_RECIPIENT_TYPE **(** [PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-183">The values pointed to by **lpulDestComps** can be used to set the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property of each recipient.</span></span> <span data-ttu-id="be0b5-184">**lpulDestComps メンバー** が NULL の場合 **、Address** メソッドは既定の受信者の種類を使用します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-184">If the **lpulDestComps** member is NULL, the **Address** method uses default recipient types.</span></span> 
    
<span data-ttu-id="be0b5-185">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="be0b5-185">**lpContRestriction**</span></span>
  
> <span data-ttu-id="be0b5-186">ダイアログ ボックスに表示できるアドレス エントリの種類を制限する [SRestriction](srestriction.md) 構造へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-186">Pointer to an [SRestriction](srestriction.md) structure that limits the type of address entries that can be displayed in the dialog box.</span></span> 
    
<span data-ttu-id="be0b5-187">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="be0b5-187">**lpHierRestriction**</span></span>
  
> <span data-ttu-id="be0b5-188">ダイアログ ボックスに表示するアドレス エントリを指定できるアドレス帳コンテナーを制限する **SRestriction** 構造へのポインター。</span><span class="sxs-lookup"><span data-stu-id="be0b5-188">Pointer to an **SRestriction** structure that limits the address book containers that can supply address entries to be displayed in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="be0b5-189">注釈</span><span class="sxs-lookup"><span data-stu-id="be0b5-189">Remarks</span></span>

<span data-ttu-id="be0b5-190">**ADRPARM 構造** は、MAPI 共通アドレス ダイアログ ボックスの外観と動作を制御するために、クライアントおよびサービス プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-190">**ADRPARM** structures are used by clients and service providers to control the appearance and behavior of the MAPI common address dialog boxes.</span></span> <span data-ttu-id="be0b5-191">[アドレス] ダイアログ ボックスには、モードレスとモーダルの 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-191">There are two varieties of the address dialog box: modeless and modal.</span></span> <span data-ttu-id="be0b5-192">**ADRPARM** 構造のメンバーの一部は、ダイアログ ボックスの両方のバージョンに適用されますが、一部のメンバーは 2 つのバージョンの 1 にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-192">Some of the members in the **ADRPARM** structure apply to both versions of the dialog box, but some only apply to one of the two versions.</span></span> <span data-ttu-id="be0b5-193">次の表は **、ADRPARM** 構造体のメンバーと、共通のアドレス ダイアログ ボックスでの使用に関する説明です。</span><span class="sxs-lookup"><span data-stu-id="be0b5-193">The following table relates the members of an **ADRPARM** structure to their use with the common address dialog boxes.</span></span> 
  
|<span data-ttu-id="be0b5-194">ADRPARM メンバー</span><span class="sxs-lookup"><span data-stu-id="be0b5-194">ADRPARM member</span></span>|<span data-ttu-id="be0b5-195">ダイアログ ボックスの種類</span><span class="sxs-lookup"><span data-stu-id="be0b5-195">Type of dialog box</span></span>|
|:-----|:-----|
|<span data-ttu-id="be0b5-196">**cbABContEntryID** と **lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="be0b5-196">**cbABContEntryID** and **lpABContEntryID**</span></span> <br/> |<span data-ttu-id="be0b5-197">モーダルとモードレス</span><span class="sxs-lookup"><span data-stu-id="be0b5-197">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="be0b5-198">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="be0b5-198">**ulFlags**</span></span> <br/> |<span data-ttu-id="be0b5-199">モーダルとモードレス</span><span class="sxs-lookup"><span data-stu-id="be0b5-199">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="be0b5-200">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="be0b5-200">**lpReserved**</span></span> <br/> |<span data-ttu-id="be0b5-201">モーダルとモードレス</span><span class="sxs-lookup"><span data-stu-id="be0b5-201">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="be0b5-202">**ulHelpContext** と **lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="be0b5-202">**ulHelpContext** and **lpszHelpFileName**</span></span> <br/> |<span data-ttu-id="be0b5-203">モーダルとモードレス</span><span class="sxs-lookup"><span data-stu-id="be0b5-203">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="be0b5-204">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="be0b5-204">**lpfnABSDI**</span></span> <br/> |<span data-ttu-id="be0b5-205">Modeless</span><span class="sxs-lookup"><span data-stu-id="be0b5-205">Modeless</span></span>  <br/> |
|<span data-ttu-id="be0b5-206">**lpfnDismiss と** **lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="be0b5-206">**lpfnDismiss** and **lpvDismissContext**</span></span> <br/> |<span data-ttu-id="be0b5-207">Modeless</span><span class="sxs-lookup"><span data-stu-id="be0b5-207">Modeless</span></span>  <br/> |
|<span data-ttu-id="be0b5-208">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="be0b5-208">**lpszCaption**</span></span> <br/> |<span data-ttu-id="be0b5-209">モーダルとモードレス</span><span class="sxs-lookup"><span data-stu-id="be0b5-209">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="be0b5-210">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="be0b5-210">**lpszNewEntryTitle**</span></span> <br/> |<span data-ttu-id="be0b5-211">Modal</span><span class="sxs-lookup"><span data-stu-id="be0b5-211">Modal</span></span>  <br/> |
|<span data-ttu-id="be0b5-212">**lpszDestWellsTitle**、 **cDestFields**、 **nDestFieldFocus**、 **lppszDestTitles**、 **および lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="be0b5-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**, and **lpulDestComps**</span></span> <br/> |<span data-ttu-id="be0b5-213">Modal</span><span class="sxs-lookup"><span data-stu-id="be0b5-213">Modal</span></span>  <br/> |
|<span data-ttu-id="be0b5-214">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="be0b5-214">**lpContRestriction**</span></span> <br/> |<span data-ttu-id="be0b5-215">モーダルとモードレス</span><span class="sxs-lookup"><span data-stu-id="be0b5-215">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="be0b5-216">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="be0b5-216">**lpHierRestriction**</span></span> <br/> |<span data-ttu-id="be0b5-217">モーダルとモードレス</span><span class="sxs-lookup"><span data-stu-id="be0b5-217">Modal and modeless</span></span>  <br/> |
   
<span data-ttu-id="be0b5-218">モードレス ダイアログ ボックスは、1 つ以上のアドレス帳コンテナーからのエントリの読み取り専用表示です。</span><span class="sxs-lookup"><span data-stu-id="be0b5-218">The modeless dialog box is a read-only display of entries from one or more address book containers.</span></span> <span data-ttu-id="be0b5-219">ダイアログ ボックスには、選択したコンテナーのすべてのエントリを表示するか、制限によって確立された条件に一致するエントリとコンテナーのみを表示できます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-219">The dialog box can display all entries from the selected containers or be limited to only those entries and containers that match criteria established by a restriction.</span></span> <span data-ttu-id="be0b5-220">**lpContRestriction** が指すコンテンツ制限は、表示されるエントリの種類を制限し **、lpHierRestriction** が指す階層制限によって、エントリを提供するコンテナーを制限できます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-220">The contents restriction pointed to by **lpContRestriction** can limit the types of entries displayed and the hierarchy restriction pointed to by **lpHierRestriction** can limit the containers providing the entries.</span></span> <span data-ttu-id="be0b5-221">ダイアログ ボックスが閉じらされた場合に呼び出し元に通知するために、MAPI は [、DISMISSMODELESS](dismissmodeless.md) プロトタイプに一致する呼び出し元によって提供される関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-221">To inform the caller when the dialog box is dismissed, MAPI invokes a function that is provided by the caller that matches the [DISMISSMODELESS](dismissmodeless.md) prototype.</span></span> <span data-ttu-id="be0b5-222">[ACCELERATEABSDI](accelerateabsdi.md)プロトタイプに一致する別の関数は、MAPI によって提供され、Windows メッセージ ループ内の呼び出し元によって呼び出され、キーボード ショートカットの作業を容易にします。</span><span class="sxs-lookup"><span data-stu-id="be0b5-222">Another function, one that matches the [ACCELERATEABSDI](accelerateabsdi.md) prototype, is provided by MAPI and invoked by the caller in the Windows message loop to facilitate the working of keyboard shortcuts.</span></span> <span data-ttu-id="be0b5-223">クライアントが [IAddrBook::Address](iaddrbook-address.md) を呼び出す場合、またはサービス プロバイダーが [IMAPISupport::Address](imapisupport-address.md)を呼び出す場合は、モードレスバージョンの MAPI アドレス ダイアログ ボックスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-223">The modeless version of the MAPI address dialog box can be displayed when clients call [IAddrBook::Address](iaddrbook-address.md) or when service providers call [IMAPISupport::Address](imapisupport-address.md).</span></span> 
  
<span data-ttu-id="be0b5-224">モーダル ダイアログ ボックスは、1 つ以上のコンテナーからのエントリの読み取り/書き込み表示です。</span><span class="sxs-lookup"><span data-stu-id="be0b5-224">The modal dialog box is a read/write display of entries from one or more containers.</span></span> <span data-ttu-id="be0b5-225">その内容は **、lpContRestriction** および **lpHierRestriction** メンバーで設定された制限によって、モードレス バージョンと同じ方法で影響を受ける可能性があります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-225">Its contents can be affected in the same manner as the modeless version by restrictions set in the **lpContRestriction** and **lpHierRestriction** members.</span></span> <span data-ttu-id="be0b5-226">コンテナー エントリを表示するリスト ボックスに加えて、モーダル ダイアログ ボックスには、ユーザーが選択したエントリを保持するための 1 ~ 3 つのテキスト ボックス コントロールを含めできます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-226">In addition to the list box displaying container entries, the modal dialog box can contain between one and three text box controls for holding entries selected by the user.</span></span> <span data-ttu-id="be0b5-227">各編集コントロールは、特定の受信者の種類や **PR_RECIPIENT_TYPEプロパティ** (MAPI_TO) に関連付MAPI_TO。</span><span class="sxs-lookup"><span data-stu-id="be0b5-227">Each edit control is associated with a particular recipient type or **PR_RECIPIENT_TYPE** property such as MAPI_TO.</span></span> <span data-ttu-id="be0b5-228">モーダル アドレス ダイアログ ボックスは **、Address** メソッドまたはクライアントが [IAddrBook::D etails](iaddrbook-details.md) とサービス プロバイダーが [IMAPISupport::D etails](imapisupport-details.md)を呼び出す場合に表示できます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-228">The modal address dialog box can be displayed by either of the **Address** methods or when clients call [IAddrBook::Details](iaddrbook-details.md) and service providers call [IMAPISupport::Details](imapisupport-details.md).</span></span> 
  
<span data-ttu-id="be0b5-229">この図には、このダイアログ ボックスの表示を制御する **ADRPARM** 構造体 **の cDestFields** メンバーが 2 に設定されているので、2 つのテキスト ボックス コントロールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="be0b5-229">This illustration includes two text box controls because the **cDestFields** member of the **ADRPARM** structure controlling the display of this dialog box is set to 2.</span></span> <span data-ttu-id="be0b5-230">**nDestFieldFocus** メンバーが 0 に設定されている場合、最初のコントロールには最初のフォーカスがあります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-230">The first control has initial focus because the **nDestFieldFocus** member is set to 0.</span></span> 
  
<span data-ttu-id="be0b5-231">**lpszNewEntryTitle** メンバーは、ボタン ラベルを選択すると、追加のダイアログ ボックスが表示されるテキストをポイントします。</span><span class="sxs-lookup"><span data-stu-id="be0b5-231">The **lpszNewEntryTitle** member points to text for a button label that, when it is selected, causes an additional dialog box to be displayed.</span></span> <span data-ttu-id="be0b5-232">通常、モーダル ダイアログ ボックスの図に示すように、ボタンには [新規]というラベルが付き、表示されるダイアログ ボックスには、プロファイル内のアドレス帳プロバイダーが作成できるすべての種類のアドレスが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-232">Typically, as is shown in the illustration of the modal dialog box, the button is labeled **New** and the dialog box that appears lists all of the types of addresses that can be created by any of the address book providers in the profile.</span></span> <span data-ttu-id="be0b5-233">クライアントは [、IAddrBook::NewEntry](iaddrbook-newentry.md)を呼び出し _、cbEidNewEntryTpl_ パラメーターに 0 を渡し、ユーザーがボタンを選択すると _lpEidNewEntryTpl_ パラメーターに NULL を渡すことによって、この [新しいエントリ] ダイアログ ボックスを表示します。 </span><span class="sxs-lookup"><span data-stu-id="be0b5-233">Clients cause this **New Entry** dialog box to be displayed by calling [IAddrBook::NewEntry](iaddrbook-newentry.md) and passing zero for the  _cbEidNewEntryTpl_ parameter and NULL for the  _lpEidNewEntryTpl_ parameter when the user selects the button.</span></span> <span data-ttu-id="be0b5-234">このダイアログ ボックスに含まれる情報は、MAPI の一時テーブルから取得されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-234">The information that is included in this dialog box comes from the MAPI one-off table.</span></span> 
  
<span data-ttu-id="be0b5-235">このダイアログ ボックス内のすべてのエントリは、特定の種類のアドレスを作成するために必要なデータを入力するテンプレートに関連付けられている。</span><span class="sxs-lookup"><span data-stu-id="be0b5-235">Every entry in this dialog box is associated with a template for entering the data required to create an address of the particular type.</span></span> <span data-ttu-id="be0b5-236">ほとんどのアドレス帳プロバイダーは、作成できるアドレスエントリのすべての種類に対して 1 つのテンプレートを提供します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-236">Most address book providers supply one template for every type of address entry they can create.</span></span> <span data-ttu-id="be0b5-237">ユーザーがこのダイアログ ボックスから選択すると、対応するテンプレートが MAPI に表示されます。</span><span class="sxs-lookup"><span data-stu-id="be0b5-237">When a user makes a selection from this dialog box, MAPI displays the corresponding template.</span></span>
  
<span data-ttu-id="be0b5-238">**ADRPARM** 構造体の **ulFlags** メンバーの最も重要な 4 ビットには、ADRPARM 構造のバージョンを識別する **バージョン番号が含** まれている。</span><span class="sxs-lookup"><span data-stu-id="be0b5-238">The most significant four bits of the **ADRPARM** structure's **ulFlags** member contain a version number identifying the version of the **ADRPARM** structure.</span></span> <span data-ttu-id="be0b5-239">現在のバージョンは 0 (ゼロ) または ADRPARM_HELP_CTX。</span><span class="sxs-lookup"><span data-stu-id="be0b5-239">The current version is 0 (zero) or ADRPARM_HELP_CTX.</span></span> <span data-ttu-id="be0b5-240">MAPI の現在の実装は、0 以外の任意のバージョンの構造体に対して失敗します。</span><span class="sxs-lookup"><span data-stu-id="be0b5-240">The current implementation of MAPI will fail for any version of the structure other than zero.</span></span> 
  
<span data-ttu-id="be0b5-241">将来のバージョンの構造は完全に異なる場合があります。バージョン 0 の構造をサポートしていない場合があります。</span><span class="sxs-lookup"><span data-stu-id="be0b5-241">Future versions of the structure may be completely different; they may not support the version-zero structure.</span></span> <span data-ttu-id="be0b5-242">**ulFlags** メンバーからバージョン番号を抽出し、それを定義されたフラグと組み合わせるには、次のマクロが用意されています。</span><span class="sxs-lookup"><span data-stu-id="be0b5-242">The following macros are provided for extracting the version number from the **ulFlags** member and for combining it with the defined flags:</span></span> 
  
- <span data-ttu-id="be0b5-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span><span class="sxs-lookup"><span data-stu-id="be0b5-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span></span> 
- <span data-ttu-id="be0b5-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span><span class="sxs-lookup"><span data-stu-id="be0b5-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span></span> 
- <span data-ttu-id="be0b5-245">**ADRPARM_HELP_CTX**</span><span class="sxs-lookup"><span data-stu-id="be0b5-245">**ADRPARM_HELP_CTX**</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be0b5-246">関連項目</span><span class="sxs-lookup"><span data-stu-id="be0b5-246">See also</span></span>

- [<span data-ttu-id="be0b5-247">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="be0b5-247">ACCELERATEABSDI</span></span>](accelerateabsdi.md)
- [<span data-ttu-id="be0b5-248">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="be0b5-248">DISMISSMODELESS</span></span>](dismissmodeless.md)
- [<span data-ttu-id="be0b5-249">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="be0b5-249">IAddrBook::Address</span></span>](iaddrbook-address.md)
- [<span data-ttu-id="be0b5-250">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="be0b5-250">IMAPISupport::Address</span></span>](imapisupport-address.md)
- [<span data-ttu-id="be0b5-251">SRestriction</span><span class="sxs-lookup"><span data-stu-id="be0b5-251">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="be0b5-252">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="be0b5-252">MAPI Structures</span></span>](mapi-structures.md)

