---
title: PidTagFolderWebViewInfo 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389961"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="9fb28-103">PidTagFolderWebViewInfo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="9fb28-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="9fb28-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fb28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fb28-105">Microsoft Outlook でフォルダーのホーム ページの URL が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fb28-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="9fb28-106">このプロパティには、 **WebViewPersistenceObject**と呼ばれるバイナリ ストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fb28-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9fb28-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="9fb28-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="9fb28-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="9fb28-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="9fb28-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="9fb28-109">Identifier:</span></span>  <br/> |<span data-ttu-id="9fb28-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="9fb28-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="9fb28-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="9fb28-111">Data type:</span></span>  <br/> |<span data-ttu-id="9fb28-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="9fb28-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="9fb28-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="9fb28-113">Area:</span></span>  <br/> |<span data-ttu-id="9fb28-114">MAPI フォルダー</span><span class="sxs-lookup"><span data-stu-id="9fb28-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fb28-115">備考</span><span class="sxs-lookup"><span data-stu-id="9fb28-115">Remarks</span></span>

<span data-ttu-id="9fb28-116">すべての Outlook フォルダーのホーム ページの URL を指定できます。</span><span class="sxs-lookup"><span data-stu-id="9fb28-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="9fb28-117">この情報は、Outlook のフォルダーの [プロパティ] ダイアログ ボックスの [**ホーム ページ**] タブからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="9fb28-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="9fb28-118">特定のポリシー設定によっては、 [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md)実装では、このフォルダーが格納されている MAPI ストアに MSCAP_SECURE_FOLDER_HOMEPAGES が報告されない場合、Outlook でホーム ページを無視して可能性がありますされます。</span><span class="sxs-lookup"><span data-stu-id="9fb28-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="9fb28-119">**Outlook Today** ] フォルダーとパブリック フォルダーの両方には、ホーム ページの Url を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="9fb28-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="9fb28-120">ただし**Outlook** today メカニズムを使用して、さまざまな管理のホーム ページの URL です。そのメカニズムは、このトピックでは説明しません。</span><span class="sxs-lookup"><span data-stu-id="9fb28-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="9fb28-121">パブリック フォルダーで定義されているホーム ページの URL、ユーザーに固有であるともあります。</span><span class="sxs-lookup"><span data-stu-id="9fb28-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="9fb28-122">ただし、その機能は、このトピックでは説明しません。</span><span class="sxs-lookup"><span data-stu-id="9fb28-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="9fb28-123">このプロパティの値は、 **WebViewPersistenceObject**と呼ばれるバイナリ ストリームです。</span><span class="sxs-lookup"><span data-stu-id="9fb28-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="9fb28-124">WebViewPersistenceObject ストリームの構造</span><span class="sxs-lookup"><span data-stu-id="9fb28-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="9fb28-125">**WebViewPersistenceObject**ストリームの構造体には、フォルダーのホーム ページの URL に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9fb28-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="9fb28-126">この構造内のデータ要素は、次の指定された順序で 1 つ別のすぐ後、リトル エンディアンのバイト順で格納されます。</span><span class="sxs-lookup"><span data-stu-id="9fb28-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9fb28-127">次の説明が表示されていないすべての Outlook でサポートされているフィールド値したがって、コードは、既存のストリームを読み取る、ときにここに記載されていないいくつかのフラグもみられます。</span><span class="sxs-lookup"><span data-stu-id="9fb28-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="9fb28-128">ただし、この説明を使用すると、Outlook を理解する**PidTagFolderWebViewInfo**プロパティの値をプログラムで作成します。</span><span class="sxs-lookup"><span data-stu-id="9fb28-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="9fb28-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="9fb28-129">_dwVersion_</span></span>
  
> <span data-ttu-id="9fb28-130">DWORD (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="9fb28-130">DWORD (4 bytes).</span></span> <span data-ttu-id="9fb28-131">構造体の形式のバージョンです。</span><span class="sxs-lookup"><span data-stu-id="9fb28-131">The version of the structure's format.</span></span> <span data-ttu-id="9fb28-132">Microsoft Office Outlook 2007 では、現在このフィールドに対してのみサポートされている値はとおりです。</span><span class="sxs-lookup"><span data-stu-id="9fb28-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="9fb28-133">**値の名前**</span><span class="sxs-lookup"><span data-stu-id="9fb28-133">**Value name**</span></span>|<span data-ttu-id="9fb28-134">**値**</span><span class="sxs-lookup"><span data-stu-id="9fb28-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9fb28-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="9fb28-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="9fb28-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="9fb28-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="9fb28-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="9fb28-137">_dwType_</span></span>
  
> <span data-ttu-id="9fb28-138">DWORD (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="9fb28-138">DWORD (4 bytes).</span></span> <span data-ttu-id="9fb28-139">ホーム ページの情報の種類です。</span><span class="sxs-lookup"><span data-stu-id="9fb28-139">The type of the home page information.</span></span> <span data-ttu-id="9fb28-140">Microsoft Office Outlook 2007 では、現在このフィールドに対してのみサポートされている値はとおりです。</span><span class="sxs-lookup"><span data-stu-id="9fb28-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="9fb28-141">**値の名前**</span><span class="sxs-lookup"><span data-stu-id="9fb28-141">**Value name**</span></span>|<span data-ttu-id="9fb28-142">**値**</span><span class="sxs-lookup"><span data-stu-id="9fb28-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9fb28-143">いる</span><span class="sxs-lookup"><span data-stu-id="9fb28-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="9fb28-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9fb28-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="9fb28-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="9fb28-145">_dwFlags_</span></span>
  
> <span data-ttu-id="9fb28-146">DWORD (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="9fb28-146">DWORD (4 bytes).</span></span> <span data-ttu-id="9fb28-147">フラグの値を 0 個以上の組み合わせと意味は次の表に記載されています。</span><span class="sxs-lookup"><span data-stu-id="9fb28-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="9fb28-148">フラグの名前。</span><span class="sxs-lookup"><span data-stu-id="9fb28-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="9fb28-149">\*\*\*\*値\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9fb28-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="9fb28-150">\*\*\*\*説明\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="9fb28-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9fb28-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="9fb28-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="9fb28-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="9fb28-152">0x00000001</span></span>  <br/> |<span data-ttu-id="9fb28-153">**このフォルダーの既定のホーム ページを表示**] チェック ボックスは、フォルダーの [プロパティ] ダイアログ ボックスの [**ホーム ページ**] タブにチェックインされました。</span><span class="sxs-lookup"><span data-stu-id="9fb28-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="9fb28-154">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="9fb28-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="9fb28-155">7 つの DWORD の要素 (28 バイトの合計) の配列です。</span><span class="sxs-lookup"><span data-stu-id="9fb28-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="9fb28-156">未使用。</span><span class="sxs-lookup"><span data-stu-id="9fb28-156">Unused.</span></span>
    
<span data-ttu-id="9fb28-157">cbData</span><span class="sxs-lookup"><span data-stu-id="9fb28-157">cbData</span></span>
  
> <span data-ttu-id="9fb28-158">ULONG (4 バイト) です。</span><span class="sxs-lookup"><span data-stu-id="9fb28-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="9fb28-159">_WzURL_データ要素のバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="9fb28-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="9fb28-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="9fb28-160">_wzURL_</span></span>
  
> <span data-ttu-id="9fb28-161">WCHAR 要素の配列。</span><span class="sxs-lookup"><span data-stu-id="9fb28-161">An array of WCHAR elements.</span></span> <span data-ttu-id="9fb28-162">ホーム ページの 0 で終わる URL 文字列の utf-16 表現。</span><span class="sxs-lookup"><span data-stu-id="9fb28-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="9fb28-163">WebViewPersistenceObject ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="9fb28-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="9fb28-164">このセクションでは、 **WebViewPersistenceObject**ストリームの例について説明します。</span><span class="sxs-lookup"><span data-stu-id="9fb28-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="9fb28-165">ストリーム ホーム ページの URL を指定する"https://www.microsoft.com"です。</span><span class="sxs-lookup"><span data-stu-id="9fb28-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="9fb28-166">**データのダンプ**</span><span class="sxs-lookup"><span data-stu-id="9fb28-166">**Data dump**</span></span>
  
<span data-ttu-id="9fb28-167">次のストリームのデータのダンプがバイナリ エディターで表示します。</span><span class="sxs-lookup"><span data-stu-id="9fb28-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="9fb28-168">**ストリームのオフセット**</span><span class="sxs-lookup"><span data-stu-id="9fb28-168">**Stream offset**</span></span>|<span data-ttu-id="9fb28-169">**データのバイト数**</span><span class="sxs-lookup"><span data-stu-id="9fb28-169">**Data bytes**</span></span>|<span data-ttu-id="9fb28-170">**ASCII データ**</span><span class="sxs-lookup"><span data-stu-id="9fb28-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9fb28-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="9fb28-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="9fb28-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="9fb28-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="9fb28-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="9fb28-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="9fb28-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="9fb28-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="9fb28-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="9fb28-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="9fb28-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="9fb28-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="9fb28-177">**WebViewPersistenceObject**ストリームのサンプル データの解析は、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="9fb28-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="9fb28-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="9fb28-178">_dwVersion_</span></span>
  
> <span data-ttu-id="9fb28-179">0x0 では、4 バイトのオフセット: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION)。</span><span class="sxs-lookup"><span data-stu-id="9fb28-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="9fb28-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="9fb28-180">_dwType_</span></span>
  
> <span data-ttu-id="9fb28-181">0x4、4 バイトのオフセット: 0x00000001 (いる)。</span><span class="sxs-lookup"><span data-stu-id="9fb28-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="9fb28-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="9fb28-182">_dwFlags_</span></span>
  
> <span data-ttu-id="9fb28-183">0x8、4 バイトのオフセット: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT)。</span><span class="sxs-lookup"><span data-stu-id="9fb28-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="9fb28-184">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="9fb28-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="9fb28-185">0 xc、28 バイトのオフセット: すべてゼロです。</span><span class="sxs-lookup"><span data-stu-id="9fb28-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="9fb28-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="9fb28-186">_cbData_</span></span>
  
> <span data-ttu-id="9fb28-187">4 バイト目の 0x28 にオフセット: 0x00000032。</span><span class="sxs-lookup"><span data-stu-id="9fb28-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="9fb28-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="9fb28-188">_wzURL_</span></span>
  
> <span data-ttu-id="9fb28-189">オフセット 0x2C、0x32 バイト: 25 WCHARs の配列です。</span><span class="sxs-lookup"><span data-stu-id="9fb28-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="9fb28-190">Unicode 0 で終わる文字列の値:"https://www.microsoft.com"です。</span><span class="sxs-lookup"><span data-stu-id="9fb28-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

