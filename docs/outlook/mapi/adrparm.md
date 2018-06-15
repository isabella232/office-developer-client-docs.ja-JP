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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: ad26cb9b77404d6470f7a8d787eb85edc5cce402
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19799667"
---
# <a name="adrparm"></a><span data-ttu-id="9b4da-103">ADRPARM</span><span class="sxs-lookup"><span data-stu-id="9b4da-103">ADRPARM</span></span>

<span data-ttu-id="9b4da-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9b4da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9b4da-105">表示と共通のアドレス] ダイアログ ボックスの動作について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-105">Describes the display and behavior of the common address dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b4da-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="9b4da-106">Header file:</span></span>  <br/> |<span data-ttu-id="9b4da-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="9b4da-107">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="9b4da-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="9b4da-108">Members</span></span>

<span data-ttu-id="9b4da-109">**cbABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="9b4da-109">**cbABContEntryID**</span></span>
  
> <span data-ttu-id="9b4da-110">**LpABContEntryID**で示されるエントリの識別子のバイト数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="9b4da-110">Count of bytes in the entry identifier pointed to by **lpABContEntryID**.</span></span>
    
<span data-ttu-id="9b4da-111">**lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="9b4da-111">**lpABContEntryID**</span></span>
  
> <span data-ttu-id="9b4da-112">最初に、[アドレス] ダイアログ ボックスに表示される受信者のアドレスのリストを提供するコンテナーのエントリの識別子へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4da-112">Pointer to the entry identifier of the container that supplies the initial list of recipient addresses that are displayed in the address dialog box.</span></span>
    
<span data-ttu-id="9b4da-113">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9b4da-113">**ulFlags**</span></span>
  
> <span data-ttu-id="9b4da-114">アドレス] ダイアログ ボックスの各種のオプションに関連付けられたフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="9b4da-114">Bitmask of flags associated with various address dialog box options.</span></span> <span data-ttu-id="9b4da-115">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-115">The following flags can be set:</span></span>
    
<span data-ttu-id="9b4da-116">AB_RESOLVE</span><span class="sxs-lookup"><span data-stu-id="9b4da-116">AB_RESOLVE</span></span>
  
> <span data-ttu-id="9b4da-117">[アドレス] ダイアログ ボックスが閉じられた後に解決されるすべての名前を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9b4da-117">Enable all names to be resolved after the address dialog box is closed.</span></span> <span data-ttu-id="9b4da-118">名前解決の処理に起因するあいまいなエントリがある場合は、それらを解決するにはユーザーの入力を求めるダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-118">If there are ambiguous entries that result from the name resolution process, a dialog box appears to prompt the user for help in resolving them.</span></span> <span data-ttu-id="9b4da-119">確実に解決されるすべての[IAddrBook::Address](iaddrbook-address.md)によって返される名前が設定されます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-119">Setting this flag guarantees that all of the names returned by [IAddrBook::Address](iaddrbook-address.md) are resolved.</span></span> 
    
<span data-ttu-id="9b4da-120">AB_SELECTONLY</span><span class="sxs-lookup"><span data-stu-id="9b4da-120">AB_SELECTONLY</span></span>
  
> <span data-ttu-id="9b4da-121">受信者の一覧については、一時アドレスの作成を無効にします。</span><span class="sxs-lookup"><span data-stu-id="9b4da-121">Disable the creation of one-off addresses for a recipient list.</span></span> <span data-ttu-id="9b4da-122">DIALOG_MODAL フラグが設定されている中で示されるように、ダイアログ ボックスはモーダルで場合にのみ、このフラグが使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-122">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span>
    
<span data-ttu-id="9b4da-123">ADDRESS_ONE</span><span class="sxs-lookup"><span data-stu-id="9b4da-123">ADDRESS_ONE</span></span>
  
> <span data-ttu-id="9b4da-124">ユーザーは、一覧から複数の受信者ではなく正確に 1 つの受信者を選択できます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-124">The user can select exactly one recipient instead of multiple recipients from a list.</span></span> <span data-ttu-id="9b4da-125">このフラグは、 **cDestFields**がゼロで、DIALOG_MODAL フラグが設定されている中で示されるように、ダイアログ ボックスはモーダルで場合にのみに有効です。</span><span class="sxs-lookup"><span data-stu-id="9b4da-125">This flag is valid only when **cDestFields** is zero and the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="9b4da-126">DIALOG_MODAL</span><span class="sxs-lookup"><span data-stu-id="9b4da-126">DIALOG_MODAL</span></span>
  
> <span data-ttu-id="9b4da-127">モーダルに表示される共通のアドレス] ダイアログ ボックスのバージョンが発生します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-127">Causes the modal version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="9b4da-128">このフラグまたは DIALOG_SDI のいずれかを設定する必要があります。それら両方は設定できません。</span><span class="sxs-lookup"><span data-stu-id="9b4da-128">Either this flag or DIALOG_SDI should be set; they cannot both be set.</span></span> 
    
<span data-ttu-id="9b4da-129">DIALOG_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="9b4da-129">DIALOG_OPTIONS</span></span>
  
> <span data-ttu-id="9b4da-130">ダイアログ ボックスに表示される**オプションの送信**] ボタンが発生します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-130">Causes the **Send Options** button to be displayed in the dialog box.</span></span> <span data-ttu-id="9b4da-131">DIALOG_MODAL フラグが設定されている中で示されるように、ダイアログ ボックスはモーダルで場合にのみ、このフラグが使用されます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-131">This flag is used only if the dialog box is modal, as indicated by the DIALOG_MODAL flag being set.</span></span> 
    
<span data-ttu-id="9b4da-132">DIALOG_SDI</span><span class="sxs-lookup"><span data-stu-id="9b4da-132">DIALOG_SDI</span></span>
  
> <span data-ttu-id="9b4da-133">モードレスに表示される共通のアドレス] ダイアログ ボックスのバージョンが発生します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-133">Causes the modeless version of the common address dialog box to be displayed.</span></span> <span data-ttu-id="9b4da-134">このフラグまたは DIALOG_MODAL のいずれかを設定する必要があります。それら両方は設定できません。</span><span class="sxs-lookup"><span data-stu-id="9b4da-134">Either this flag or DIALOG_MODAL should be set; they cannot both be set.</span></span> <span data-ttu-id="9b4da-135">DIALOG_SDI フラグは無視されます、Outlook 以外のクライアントと、ダイアログ ボックスのモーダル バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-135">The DIALOG_SDI flag is ignored for non-Outlook clients, and the modal version of the dialog box will be displayed.</span></span> <span data-ttu-id="9b4da-136">その結果、ハンドルへのポインターを期待していない[IAddrBook::Address](iaddrbook-address.md)の_lpulUIParam_パラメーターにします。</span><span class="sxs-lookup"><span data-stu-id="9b4da-136">Consequently, a pointer to a handle should not be expected in the  _lpulUIParam_ parameter of [IAddrBook::Address](iaddrbook-address.md).</span></span>
    
<span data-ttu-id="9b4da-137">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="9b4da-137">**lpReserved**</span></span>
  
> <span data-ttu-id="9b4da-138">予約済み、0 でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9b4da-138">Reserved, must be zero.</span></span>
    
<span data-ttu-id="9b4da-139">**ulHelpContext**</span><span class="sxs-lookup"><span data-stu-id="9b4da-139">**ulHelpContext**</span></span>
  
> <span data-ttu-id="9b4da-140">**ヘルプ**を最初に表示されますユーザーが、[アドレス] ダイアログ ボックスで [ヘルプ] ボタンをクリックしたときにコンテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-140">Specifies the context within **Help** that will first be shown when the user clicks the Help button in the address dialog box.</span></span> 
    
<span data-ttu-id="9b4da-141">**lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="9b4da-141">**lpszHelpFileName**</span></span>
  
> <span data-ttu-id="9b4da-142">[アドレス] ダイアログ ボックスに関連付けられるヘルプ ファイルの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4da-142">Pointer to the name of a Help file that will be associated with the address dialog box.</span></span> <span data-ttu-id="9b4da-143">**UlHelpContext**とは、 **lpszHelpFileName**メンバーを使用して、Windows**ヘルプ**関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-143">The **lpszHelpFileName** member is used together with **ulHelpContext** to call the Windows **WinHelp** function.</span></span> 
    
<span data-ttu-id="9b4da-144">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="9b4da-144">**lpfnABSDI**</span></span>
  
> <span data-ttu-id="9b4da-145">[ACCELERATEABSDI](accelerateabsdi.md)のプロトタイプには MAPI 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4da-145">Pointer to a MAPI function based on the [ACCELERATEABSDI](accelerateabsdi.md) prototype or NULL.</span></span> <span data-ttu-id="9b4da-146">このメンバーは、モードレス ダイアログ ボックスでのみのバージョンに適用されます DIALOG_SDI フラグが設定されている中で示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="9b4da-146">This member applies to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="9b4da-147">[IAddrBook::Address](iaddrbook-address.md)に渡すための**ADRPARM**構造体を構築するクライアントは、 **lpfnABSDI**メンバーを NULL に設定する必要があります常に。</span><span class="sxs-lookup"><span data-stu-id="9b4da-147">Clients building an **ADRPARM** structure to pass to [IAddrBook::Address](iaddrbook-address.md) must always set the **lpfnABSDI** member to NULL.</span></span> <span data-ttu-id="9b4da-148">DIALOG_SDI フラグが設定されている場合 MAPI は後でその設定に有効な関数を返す前に。</span><span class="sxs-lookup"><span data-stu-id="9b4da-148">If the DIALOG_SDI flag is set, MAPI will then set it to a valid function before returning.</span></span> <span data-ttu-id="9b4da-149">クライアントは、アドレスでアクセラレータが] ダイアログ ボックスの作業を予約するかどうかを確認するメッセージ ループ内からこの関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-149">Clients call this function from in their message loop to make sure that accelerators in the address book dialog box work.</span></span> <span data-ttu-id="9b4da-150">ダイアログ ボックスを閉じるし、MAPI は、 **lpfnDismiss**のメンバーで指定された関数を呼び出す、クライアントする必要があります、メッセージ ループから**ACCELERATEABSDI**関数を外します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-150">When the dialog box is dismissed and MAPI calls the function pointed to by the **lpfnDismiss** member, clients should unhook the **ACCELERATEABSDI** function from their message loop.</span></span> 
    
<span data-ttu-id="9b4da-151">**lpfnDismiss**</span><span class="sxs-lookup"><span data-stu-id="9b4da-151">**lpfnDismiss**</span></span>
  
> <span data-ttu-id="9b4da-152">[DISMISSMODELESS](dismissmodeless.md)のプロトタイプでは関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4da-152">Pointer to a function based on the [DISMISSMODELESS](dismissmodeless.md) prototype or NULL.</span></span> <span data-ttu-id="9b4da-153">このメンバーは、モードレス ダイアログ ボックスでのみのバージョンにのみ適用されます DIALOG_SDI フラグが設定されている中で示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="9b4da-153">This member applies only to the modeless version of the dialog box only, as indicated by the DIALOG_SDI flag being set.</span></span> <span data-ttu-id="9b4da-154">MAPI 関数を呼び出す**DISMISSMODELESS**ユーザーが、アドレスのモードレス ダイアログ ボックスを閉じると、 **IAddrBook::Address**ダイアログ ボックスがアクティブではないことを呼び出すクライアントに通知します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-154">MAPI calls the **DISMISSMODELESS** function when the user dismisses the modeless address dialog box, informing a client calling **IAddrBook::Address** that the dialog box is no longer active.</span></span> 
    
<span data-ttu-id="9b4da-155">**lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="9b4da-155">**lpvDismissContext**</span></span>
  
> <span data-ttu-id="9b4da-156">**LpfnDismiss**メンバーが指す、 **DISMISSMODELESS**関数に渡されるコンテキスト情報へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="9b4da-156">Pointer to context information to be passed to the **DISMISSMODELESS** function pointed to by the **lpfnDismiss** member.</span></span> <span data-ttu-id="9b4da-157">このメンバーは、DIALOG_SDI フラグが設定されている中で示されるように、モードレス ダイアログ ボックスのバージョンにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-157">This member applies only to the modeless version of the dialog box, as indicated by the DIALOG_SDI flag being set.</span></span> 
    
<span data-ttu-id="9b4da-158">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="9b4da-158">**lpszCaption**</span></span>
  
> <span data-ttu-id="9b4da-159">共通のアドレス] ダイアログ ボックスのタイトルとして使用する文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4da-159">Pointer to text to be used as the title for the common address dialog box.</span></span>
    
<span data-ttu-id="9b4da-160">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="9b4da-160">**lpszNewEntryTitle**</span></span>
  
> <span data-ttu-id="9b4da-161">**[新しいエントリ**] ダイアログ ボックスまたは別のダイアログ ボックスのいずれかを起動するボタンのボタンのラベルとして使用する文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4da-161">Pointer to text to be used as the button label for the button that invokes either the **New Entry** dialog box or another dialog box.</span></span> 
    
<span data-ttu-id="9b4da-162">**lpszDestWellsTitle**</span><span class="sxs-lookup"><span data-stu-id="9b4da-162">**lpszDestWellsTitle**</span></span>
  
> <span data-ttu-id="9b4da-163">共通のアドレス] ダイアログ ボックスのモーダル バージョンに表示される受信者のテキスト ボックス コントロールのタイトルとして使用する文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4da-163">Pointer to text to be used as a title for the recipient text box controls that can appear in the modal version of the common address dialog box.</span></span> <span data-ttu-id="9b4da-164">モードレス ダイアログ ボックスのこのメンバーは使用されません。</span><span class="sxs-lookup"><span data-stu-id="9b4da-164">This member is not used for modeless dialog boxes.</span></span> 
    
<span data-ttu-id="9b4da-165">**cDestFields**</span><span class="sxs-lookup"><span data-stu-id="9b4da-165">**cDestFields**</span></span>
  
> <span data-ttu-id="9b4da-166">受信者内のテキスト ボックス コントロール、[アドレス] ダイアログ ボックスまたはダイアログ ボックスがモードレスの場合にゼロのモーダル バージョンの数です。</span><span class="sxs-lookup"><span data-stu-id="9b4da-166">Count of recipient text box controls in the modal version of the address dialog box, or zero if the dialog box is modeless.</span></span> <span data-ttu-id="9b4da-167">[アドレス] ダイアログ ボックスは、次の条件に該当する場合にのみを参照するために開いています。</span><span class="sxs-lookup"><span data-stu-id="9b4da-167">The address dialog box is open for browsing only when the following conditions are true:</span></span> 
    
  - <span data-ttu-id="9b4da-168">**CDestFields**メンバーは、0 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="9b4da-168">The **cDestFields** member is set to zero.</span></span> 
    
  - <span data-ttu-id="9b4da-169">DIALOG_BOX フラグが設定されています。</span><span class="sxs-lookup"><span data-stu-id="9b4da-169">The DIALOG_BOX flag is set.</span></span>
    
  - <span data-ttu-id="9b4da-170">ADDRESS_ONE フラグが設定されていません。</span><span class="sxs-lookup"><span data-stu-id="9b4da-170">The ADDRESS_ONE flag is not set.</span></span>
    
  <span data-ttu-id="9b4da-171">**CDestFields**を 0 XFFFFFFFF に設定すると、MAPI を作成するように受信者のテキストの既定の数] ボックスのコントロールを意味します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-171">Setting **cDestFields** to 0XFFFFFFFF implies that MAPI should create the default number of recipient text box controls.</span></span> <span data-ttu-id="9b4da-172">この例では、 **lppszDestTitles**と**lpulDestComps**のメンバーは NULL にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b4da-172">In this case, the **lppszDestTitles** and **lpulDestComps** members must be NULL.</span></span> 
    
<span data-ttu-id="9b4da-173">**nDestFieldFocus**</span><span class="sxs-lookup"><span data-stu-id="9b4da-173">**nDestFieldFocus**</span></span>
  
> <span data-ttu-id="9b4da-174">モーダル ダイアログ ボックスのバージョンが表示されたら、初期フォーカスを持っている必要がありますが、特定のテキスト ボックス コントロールを示します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-174">Indicates the particular text box control that should have the initial focus when the modal version of the dialog box appears.</span></span> <span data-ttu-id="9b4da-175">この値は、0 から 1 を引いた**cDestFields**の値の間にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b4da-175">This value must be between 0 and the value of **cDestFields** minus 1.</span></span> 
    
<span data-ttu-id="9b4da-176">**lppszDestTitles**</span><span class="sxs-lookup"><span data-stu-id="9b4da-176">**lppszDestTitles**</span></span>
  
> <span data-ttu-id="9b4da-177">[アドレス] ダイアログ ボックスのモーダル バージョンで表示されているテキスト ボックス コントロールのそれぞれに関連付けられたボタンのラベルの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4da-177">Pointer to an array of labels for buttons associated with each of the text box controls that are displayed in the modal version of the address dialog box.</span></span> <span data-ttu-id="9b4da-178">**CDestFields**メンバーの値は、配列に含まれているラベルの数を示します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-178">The value of the **cDestFields** member indicates the number of labels included in the array.</span></span> <span data-ttu-id="9b4da-179">**LppszDestTitles**メンバーが NULL の場合は、**アドレス**のメソッドは、既定のタイトルを使用します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-179">If the **lppszDestTitles** member is NULL, the **Address** method uses default titles.</span></span> 
    
<span data-ttu-id="9b4da-180">**lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="9b4da-180">**lpulDestComps**</span></span>
  
> <span data-ttu-id="9b4da-181">各テキスト ボックス コントロールに関連付けられている MAPI_TO、MAPI_CC、MAPI_BCC などの受信者の種類の値の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4da-181">Pointer to an array of recipient type values, such as MAPI_TO, MAPI_CC, and MAPI_BCC, that is associated with each text box control.</span></span> <span data-ttu-id="9b4da-182">**CDestFields**メンバーの値は、配列に含まれる受信者の種類の数を示します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-182">The value of the **CDestFields** member indicates the number of recipient types included in the array.</span></span> <span data-ttu-id="9b4da-183">**LpulDestComps**が指す値は、各受信者の**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) のプロパティを設定するのには使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-183">The values pointed to by **lpulDestComps** can be used to set the **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) property of each recipient.</span></span> <span data-ttu-id="9b4da-184">**LpulDestComps**メンバーが NULL の場合は、**アドレス**のメソッドは、既定の受信者の種類を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-184">If the **lpulDestComps** member is NULL, the **Address** method uses default recipient types.</span></span> 
    
<span data-ttu-id="9b4da-185">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="9b4da-185">**lpContRestriction**</span></span>
  
> <span data-ttu-id="9b4da-186">ダイアログ ボックスで表示されるアドレス エントリの種類を制限する[SRestriction](srestriction.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4da-186">Pointer to an [SRestriction](srestriction.md) structure that limits the type of address entries that can be displayed in the dialog box.</span></span> 
    
<span data-ttu-id="9b4da-187">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="9b4da-187">**lpHierRestriction**</span></span>
  
> <span data-ttu-id="9b4da-188">ダイアログ ボックスに表示されるアドレスのエントリを提供できるアドレス帳コンテナーを制限する**SRestriction**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9b4da-188">Pointer to an **SRestriction** structure that limits the address book containers that can supply address entries to be displayed in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9b4da-189">Remarks</span><span class="sxs-lookup"><span data-stu-id="9b4da-189">Remarks</span></span>

<span data-ttu-id="9b4da-190">コモン アドレス] ダイアログ ボックスの動作と外観を制御するクライアントとサービス ・ プロバイダーによって使用されるは、 **ADRPARM**構造体です。</span><span class="sxs-lookup"><span data-stu-id="9b4da-190">**ADRPARM** structures are used by clients and service providers to control the appearance and behavior of the MAPI common address dialog boxes.</span></span> <span data-ttu-id="9b4da-191">[アドレス] ダイアログ ボックスの 2 つの種類があります: モードレスとモーダルです。</span><span class="sxs-lookup"><span data-stu-id="9b4da-191">There are two varieties of the address dialog box: modeless and modal.</span></span> <span data-ttu-id="9b4da-192">**ADRPARM**構造体のメンバーのいくつかのダイアログ ボックスの両方のバージョンに適用しますが、いくつかは、2 つのバージョンのいずれかにのみ適用します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-192">Some of the members in the **ADRPARM** structure apply to both versions of the dialog box, but some only apply to one of the two versions.</span></span> <span data-ttu-id="9b4da-193">次の表には、共通のアドレス] ダイアログ ボックスで、使用する**ADRPARM**構造体のメンバーが関連しています。</span><span class="sxs-lookup"><span data-stu-id="9b4da-193">The following table relates the members of an **ADRPARM** structure to their use with the common address dialog boxes.</span></span> 
  
|<span data-ttu-id="9b4da-194">ADRPARM メンバー</span><span class="sxs-lookup"><span data-stu-id="9b4da-194">ADRPARM member</span></span>|<span data-ttu-id="9b4da-195">ダイアログ ボックスの種類</span><span class="sxs-lookup"><span data-stu-id="9b4da-195">Type of dialog box</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b4da-196">**cbABContEntryID**と**lpABContEntryID**</span><span class="sxs-lookup"><span data-stu-id="9b4da-196">**cbABContEntryID** and **lpABContEntryID**</span></span> <br/> |<span data-ttu-id="9b4da-197">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="9b4da-197">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="9b4da-198">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="9b4da-198">**ulFlags**</span></span> <br/> |<span data-ttu-id="9b4da-199">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="9b4da-199">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="9b4da-200">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="9b4da-200">**lpReserved**</span></span> <br/> |<span data-ttu-id="9b4da-201">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="9b4da-201">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="9b4da-202">**ulHelpContext**と**lpszHelpFileName**</span><span class="sxs-lookup"><span data-stu-id="9b4da-202">**ulHelpContext** and **lpszHelpFileName**</span></span> <br/> |<span data-ttu-id="9b4da-203">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="9b4da-203">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="9b4da-204">**lpfnABSDI**</span><span class="sxs-lookup"><span data-stu-id="9b4da-204">**lpfnABSDI**</span></span> <br/> |<span data-ttu-id="9b4da-205">モードレス</span><span class="sxs-lookup"><span data-stu-id="9b4da-205">Modeless</span></span>  <br/> |
|<span data-ttu-id="9b4da-206">**lpfnDismiss**と**lpvDismissContext**</span><span class="sxs-lookup"><span data-stu-id="9b4da-206">**lpfnDismiss** and **lpvDismissContext**</span></span> <br/> |<span data-ttu-id="9b4da-207">モードレス</span><span class="sxs-lookup"><span data-stu-id="9b4da-207">Modeless</span></span>  <br/> |
|<span data-ttu-id="9b4da-208">**lpszCaption**</span><span class="sxs-lookup"><span data-stu-id="9b4da-208">**lpszCaption**</span></span> <br/> |<span data-ttu-id="9b4da-209">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="9b4da-209">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="9b4da-210">**lpszNewEntryTitle**</span><span class="sxs-lookup"><span data-stu-id="9b4da-210">**lpszNewEntryTitle**</span></span> <br/> |<span data-ttu-id="9b4da-211">モーダル</span><span class="sxs-lookup"><span data-stu-id="9b4da-211">Modal</span></span>  <br/> |
|<span data-ttu-id="9b4da-212">**lpszDestWellsTitle**、 **cDestFields**、 **nDestFieldFocus**、 **lppszDestTitles**、および**lpulDestComps**</span><span class="sxs-lookup"><span data-stu-id="9b4da-212">**lpszDestWellsTitle**, **cDestFields**, **nDestFieldFocus**, **lppszDestTitles**, and **lpulDestComps**</span></span> <br/> |<span data-ttu-id="9b4da-213">モーダル</span><span class="sxs-lookup"><span data-stu-id="9b4da-213">Modal</span></span>  <br/> |
|<span data-ttu-id="9b4da-214">**lpContRestriction**</span><span class="sxs-lookup"><span data-stu-id="9b4da-214">**lpContRestriction**</span></span> <br/> |<span data-ttu-id="9b4da-215">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="9b4da-215">Modal and modeless</span></span>  <br/> |
|<span data-ttu-id="9b4da-216">**lpHierRestriction**</span><span class="sxs-lookup"><span data-stu-id="9b4da-216">**lpHierRestriction**</span></span> <br/> |<span data-ttu-id="9b4da-217">モーダルおよびモードレス</span><span class="sxs-lookup"><span data-stu-id="9b4da-217">Modal and modeless</span></span>  <br/> |
   
<span data-ttu-id="9b4da-218">モードレス ダイアログ ボックスは、1 つまたは複数のアドレス帳コンテナーからのエントリの読み取り専用表示です。</span><span class="sxs-lookup"><span data-stu-id="9b4da-218">The modeless dialog box is a read-only display of entries from one or more address book containers.</span></span> <span data-ttu-id="9b4da-219">ダイアログ ボックスでは、選択したコンテナーからすべてのエントリを表示したり、エントリと、制限が設定した基準に一致するコンテナーのみに限定することができます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-219">The dialog box can display all entries from the selected containers or be limited to only those entries and containers that match criteria established by a restriction.</span></span> <span data-ttu-id="9b4da-220">**LpContRestriction**が指す内容の制限が表示されるエントリの種類を制限し、 **lpHierRestriction**で示される階層の制限は、コンテナーのエントリを提供することを制限できます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-220">The contents restriction pointed to by **lpContRestriction** can limit the types of entries displayed and the hierarchy restriction pointed to by **lpHierRestriction** can limit the containers providing the entries.</span></span> <span data-ttu-id="9b4da-221">ダイアログ ボックスを終了したときに呼び出し元に通知をするには、MAPI は、 [DISMISSMODELESS](dismissmodeless.md)のプロトタイプに一致する呼び出し元によって提供される関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-221">To inform the caller when the dialog box is dismissed, MAPI invokes a function that is provided by the caller that matches the [DISMISSMODELESS](dismissmodeless.md) prototype.</span></span> <span data-ttu-id="9b4da-222">[ACCELERATEABSDI](accelerateabsdi.md)プロトタイプに一致する別の関数は MAPI によって提供され、キーボード ショート カットの作業を容易にする Windows メッセージ ループの呼び出し元によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-222">Another function, one that matches the [ACCELERATEABSDI](accelerateabsdi.md) prototype, is provided by MAPI and invoked by the caller in the Windows message loop to facilitate the working of keyboard shortcuts.</span></span> <span data-ttu-id="9b4da-223">クライアントは、 [IAddrBook::Address](iaddrbook-address.md)を呼び出すとき、またはサービス プロバイダーは、 [IMAPISupport::Address](imapisupport-address.md)を呼び出すと、モードレスのバージョンの MAPI アドレス] ダイアログ ボックスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-223">The modeless version of the MAPI address dialog box can be displayed when clients call [IAddrBook::Address](iaddrbook-address.md) or when service providers call [IMAPISupport::Address](imapisupport-address.md).</span></span> 
  
<span data-ttu-id="9b4da-224">モーダル ダイアログ ボックスは、1 つまたは複数のコンテナーからのエントリの読み取り/書き込みの表示です。</span><span class="sxs-lookup"><span data-stu-id="9b4da-224">The modal dialog box is a read/write display of entries from one or more containers.</span></span> <span data-ttu-id="9b4da-225">モードレス バージョンの制限を設定**lpContRestriction**と**lpHierRestriction**のメンバーと同様にその内容が適用されます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-225">Its contents can be affected in the same manner as the modeless version by restrictions set in the **lpContRestriction** and **lpHierRestriction** members.</span></span> <span data-ttu-id="9b4da-226">コンテナーのエントリを表示するボックスの一覧のほか、モーダル ダイアログ ボックスがユーザーによって選択されたエントリを保持するために、1 つと 3 つのテキスト ボックス コントロールの間で含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-226">In addition to the list box displaying container entries, the modal dialog box can contain between one and three text box controls for holding entries selected by the user.</span></span> <span data-ttu-id="9b4da-227">各エディット コントロールは、特定の受信者の種類や MAPI_TO などの**PR_RECIPIENT_TYPE**プロパティに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-227">Each edit control is associated with a particular recipient type or **PR_RECIPIENT_TYPE** property such as MAPI_TO.</span></span> <span data-ttu-id="9b4da-228">クライアントは、 [IAddrBook::Details](iaddrbook-details.md)を呼び出すし、サービス プロバイダーは、 [IMAPISupport::Details](imapisupport-details.md)を呼び出すとき、または**アドレス**の方法のいずれかで、作業ウィンドウ固定のアドレス] ダイアログ ボックスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-228">The modal address dialog box can be displayed by either of the **Address** methods or when clients call [IAddrBook::Details](iaddrbook-details.md) and service providers call [IMAPISupport::Details](imapisupport-details.md).</span></span> 
  
<span data-ttu-id="9b4da-229">**CDestFields** 、 **ADRPARM**構造体のメンバーは、このダイアログ ボックスの表示を制御することが 2 に設定されているために、この図には 2 つのテキスト ボックス コントロールが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-229">This illustration includes two text box controls because the **cDestFields** member of the **ADRPARM** structure controlling the display of this dialog box is set to 2.</span></span> <span data-ttu-id="9b4da-230">最初のコントロールでは、 **nDestFieldFocus**メンバーは 0 に設定されているために初期フォーカスがあります。</span><span class="sxs-lookup"><span data-stu-id="9b4da-230">The first control has initial focus because the **nDestFieldFocus** member is set to 0.</span></span> 
  
<span data-ttu-id="9b4da-231">**LpszNewEntryTitle**メンバーを選択すると、追加のダイアログ ボックスを表示すると、ボタンのラベルのテキストをポイントします。</span><span class="sxs-lookup"><span data-stu-id="9b4da-231">The **lpszNewEntryTitle** member points to text for a button label that, when it is selected, causes an additional dialog box to be displayed.</span></span> <span data-ttu-id="9b4da-232">通常は、ボタンの**新しい**ラベルは、図のように、モーダル ダイアログ ボックスのし、表示されるダイアログ ボックスのすべてのプロファイルで、アドレス帳プロバイダーのいずれかで作成可能なアドレスの種類の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-232">Typically, as is shown in the illustration of the modal dialog box, the button is labeled **New** and the dialog box that appears lists all of the types of addresses that can be created by any of the address book providers in the profile.</span></span> <span data-ttu-id="9b4da-233">クライアントには、 [IAddrBook::NewEntry](iaddrbook-newentry.md)を呼び出すと、ユーザーがボタンを選択した場合、 _cbEidNewEntryTpl_パラメーターの 0 と_lpEidNewEntryTpl_のパラメーターに NULL を渡すことによって表示されるこの**新しいエントリ**のダイアログ ボックスがあります。</span><span class="sxs-lookup"><span data-stu-id="9b4da-233">Clients cause this **New Entry** dialog box to be displayed by calling [IAddrBook::NewEntry](iaddrbook-newentry.md) and passing zero for the  _cbEidNewEntryTpl_ parameter and NULL for the  _lpEidNewEntryTpl_ parameter when the user selects the button.</span></span> <span data-ttu-id="9b4da-234">このダイアログ ボックスに含まれる情報は、MAPI の一時テーブルから取得されます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-234">The information that is included in this dialog box comes from the MAPI one-off table.</span></span> 
  
<span data-ttu-id="9b4da-235">このダイアログ ボックス内のすべてのエントリは、特定の種類のアドレスを作成するために必要なデータを入力するためのテンプレートに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-235">Every entry in this dialog box is associated with a template for entering the data required to create an address of the particular type.</span></span> <span data-ttu-id="9b4da-236">ほとんどのアドレス帳プロバイダーでは、アドレスのエントリを作成することのすべての種類の 1 つのテンプレートを提供します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-236">Most address book providers supply one template for every type of address entry they can create.</span></span> <span data-ttu-id="9b4da-237">このダイアログ ボックスから選択を行うと、MAPI には、対応するテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9b4da-237">When a user makes a selection from this dialog box, MAPI displays the corresponding template.</span></span>
  
<span data-ttu-id="9b4da-238">**ADRPARM**構造体の**ulFlags**メンバーの最上位 4 ビットには、 **ADRPARM**構造体のバージョンを識別するバージョン番号が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9b4da-238">The most significant four bits of the **ADRPARM** structure's **ulFlags** member contain a version number identifying the version of the **ADRPARM** structure.</span></span> <span data-ttu-id="9b4da-239">現在のバージョンは、0 (ゼロ) または ADRPARM_HELP_CTX。</span><span class="sxs-lookup"><span data-stu-id="9b4da-239">The current version is 0 (zero) or ADRPARM_HELP_CTX.</span></span> <span data-ttu-id="9b4da-240">MAPI の現在の実装は、0 以外の構造体のすべてのバージョンで失敗します。</span><span class="sxs-lookup"><span data-stu-id="9b4da-240">The current implementation of MAPI will fail for any version of the structure other than zero.</span></span> 
  
<span data-ttu-id="9b4da-241">構造体の将来のバージョンが完全に別の可能性があります。バージョン 0 の構造体ができません。</span><span class="sxs-lookup"><span data-stu-id="9b4da-241">Future versions of the structure may be completely different; they may not support the version-zero structure.</span></span> <span data-ttu-id="9b4da-242">**UlFlags**メンバーからバージョン番号を抽出するため、定義済みのフラグを組み合わせることで、次のマクロが用意されています。</span><span class="sxs-lookup"><span data-stu-id="9b4da-242">The following macros are provided for extracting the version number from the **ulFlags** member and for combining it with the defined flags:</span></span> 
  
- <span data-ttu-id="9b4da-243">**GET_ADRPARM_VERSION**(_ulFlags_)</span><span class="sxs-lookup"><span data-stu-id="9b4da-243">**GET_ADRPARM_VERSION** (_ulFlags_)</span></span> 
- <span data-ttu-id="9b4da-244">**SET_ADRPARM_VERSION**(_ulFlags_、_ ulVersion _)</span><span class="sxs-lookup"><span data-stu-id="9b4da-244">**SET_ADRPARM_VERSION** (_ulFlags_, _ ulVersion _)</span></span> 
- <span data-ttu-id="9b4da-245">**ADRPARM_HELP_CTX**</span><span class="sxs-lookup"><span data-stu-id="9b4da-245">**ADRPARM_HELP_CTX**</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9b4da-246">関連項目</span><span class="sxs-lookup"><span data-stu-id="9b4da-246">See also</span></span>

- [<span data-ttu-id="9b4da-247">ACCELERATEABSDI</span><span class="sxs-lookup"><span data-stu-id="9b4da-247">ACCELERATEABSDI</span></span>](accelerateabsdi.md)
- [<span data-ttu-id="9b4da-248">DISMISSMODELESS</span><span class="sxs-lookup"><span data-stu-id="9b4da-248">DISMISSMODELESS</span></span>](dismissmodeless.md)
- [<span data-ttu-id="9b4da-249">IAddrBook::Address</span><span class="sxs-lookup"><span data-stu-id="9b4da-249">IAddrBook::Address</span></span>](iaddrbook-address.md)
- [<span data-ttu-id="9b4da-250">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="9b4da-250">IMAPISupport::Address</span></span>](imapisupport-address.md)
- [<span data-ttu-id="9b4da-251">SRestriction</span><span class="sxs-lookup"><span data-stu-id="9b4da-251">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="9b4da-252">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="9b4da-252">MAPI Structures</span></span>](mapi-structures.md)

