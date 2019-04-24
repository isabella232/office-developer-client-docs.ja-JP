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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316311"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="5092a-103">PidTagFolderWebViewInfo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="5092a-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="5092a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5092a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5092a-105">Microsoft Outlook のフォルダーのホームページの URL が保存されています。</span><span class="sxs-lookup"><span data-stu-id="5092a-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="5092a-106">このプロパティには、 **WebViewPersistenceObject**と呼ばれるバイナリストリームが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5092a-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5092a-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="5092a-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="5092a-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="5092a-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="5092a-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="5092a-109">Identifier:</span></span>  <br/> |<span data-ttu-id="5092a-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="5092a-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="5092a-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="5092a-111">Data type:</span></span>  <br/> |<span data-ttu-id="5092a-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5092a-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5092a-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="5092a-113">Area:</span></span>  <br/> |<span data-ttu-id="5092a-114">MAPI フォルダー</span><span class="sxs-lookup"><span data-stu-id="5092a-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5092a-115">解説</span><span class="sxs-lookup"><span data-stu-id="5092a-115">Remarks</span></span>

<span data-ttu-id="5092a-116">ホームページの URL は任意の Outlook フォルダーに指定できます。</span><span class="sxs-lookup"><span data-stu-id="5092a-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="5092a-117">この情報には、Outlook でフォルダーの [プロパティ] ダイアログボックスの [**ホームページ**] タブからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5092a-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="5092a-118">特定のポリシー設定によっては、ホームページが Outlook で無視されることがあります。このフォルダーを含む MAPI ストアでは、 [imscapabilities:: getcapabilities](pidtagfolderwebviewinfo-cannonical-property.md)実装の MSCAP_SECURE_FOLDER_HOMEPAGES が報告されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="5092a-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="5092a-119">**Outlook Today**フォルダーとパブリックフォルダーの両方に、ホームページの url を設定できます。</span><span class="sxs-lookup"><span data-stu-id="5092a-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="5092a-120">ただし、 **Outlook Today**フォルダーでは、ホームページの URL を管理するために別のメカニズムを使用しています。このトピックでは、このメカニズムについては説明しません。</span><span class="sxs-lookup"><span data-stu-id="5092a-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="5092a-121">パブリックフォルダーには、ユーザーに固有のホームページの URL が定義されている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="5092a-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="5092a-122">ただし、このトピックではこの機能については説明しません。</span><span class="sxs-lookup"><span data-stu-id="5092a-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="5092a-123">このプロパティの値は、 **WebViewPersistenceObject**と呼ばれるバイナリストリームです。</span><span class="sxs-lookup"><span data-stu-id="5092a-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="5092a-124">WebViewPersistenceObject Stream 構造</span><span class="sxs-lookup"><span data-stu-id="5092a-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="5092a-125">**WebViewPersistenceObject** stream 構造には、フォルダーのホームページの URL に関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5092a-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="5092a-126">この構造体の Data 要素は、次の指定された順序で、すぐに、リトルエンディアンバイト順に格納されます。</span><span class="sxs-lookup"><span data-stu-id="5092a-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5092a-127">次の説明では、Outlook でサポートされているすべてのフィールド値が一覧表示されない場合があります。そのため、コードで既存のストリームを読み取る場合、ここに記載されていないフラグも検索されることがあります。</span><span class="sxs-lookup"><span data-stu-id="5092a-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="5092a-128">ただし、この説明を使用して、Outlook が認識する**PidTagFolderWebViewInfo**プロパティの値をプログラムで作成することができます。</span><span class="sxs-lookup"><span data-stu-id="5092a-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="5092a-129">_dwversion_</span><span class="sxs-lookup"><span data-stu-id="5092a-129">_dwVersion_</span></span>
  
> <span data-ttu-id="5092a-130">DWORD (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="5092a-130">DWORD (4 bytes).</span></span> <span data-ttu-id="5092a-131">構造体の形式のバージョン。</span><span class="sxs-lookup"><span data-stu-id="5092a-131">The version of the structure's format.</span></span> <span data-ttu-id="5092a-132">Microsoft Office Outlook 2007 の場合、このフィールドでサポートされている値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5092a-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="5092a-133">**値の名前**</span><span class="sxs-lookup"><span data-stu-id="5092a-133">**Value name**</span></span>|<span data-ttu-id="5092a-134">**値**</span><span class="sxs-lookup"><span data-stu-id="5092a-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5092a-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="5092a-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="5092a-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5092a-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="5092a-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="5092a-137">_dwType_</span></span>
  
> <span data-ttu-id="5092a-138">DWORD (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="5092a-138">DWORD (4 bytes).</span></span> <span data-ttu-id="5092a-139">ホームページ情報の種類を示します。</span><span class="sxs-lookup"><span data-stu-id="5092a-139">The type of the home page information.</span></span> <span data-ttu-id="5092a-140">Microsoft Office Outlook 2007 の場合、このフィールドでサポートされている値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5092a-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="5092a-141">**値の名前**</span><span class="sxs-lookup"><span data-stu-id="5092a-141">**Value name**</span></span>|<span data-ttu-id="5092a-142">**値**</span><span class="sxs-lookup"><span data-stu-id="5092a-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5092a-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="5092a-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="5092a-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5092a-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="5092a-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="5092a-145">_dwFlags_</span></span>
  
> <span data-ttu-id="5092a-146">DWORD (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="5092a-146">DWORD (4 bytes).</span></span> <span data-ttu-id="5092a-147">次の表に、値と意味を含む0個以上のフラグの組み合わせを示します。</span><span class="sxs-lookup"><span data-stu-id="5092a-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="5092a-148">フラグ名 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="5092a-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="5092a-149">\*\*\*\*値\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5092a-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="5092a-150">\*\*\*\*説明\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5092a-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5092a-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="5092a-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="5092a-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5092a-152">0x00000001</span></span>  <br/> |<span data-ttu-id="5092a-153">フォルダーの [プロパティ] ダイアログボックスの [**ホームページ**] タブで、[**このフォルダーに既定でホームページを表示**する] チェックボックスがオンになっています。</span><span class="sxs-lookup"><span data-stu-id="5092a-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="5092a-154">_dwunused [7]_</span><span class="sxs-lookup"><span data-stu-id="5092a-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="5092a-155">7個の DWORD 要素の配列 (合計28バイト)。</span><span class="sxs-lookup"><span data-stu-id="5092a-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="5092a-156">使用.</span><span class="sxs-lookup"><span data-stu-id="5092a-156">Unused.</span></span>
    
<span data-ttu-id="5092a-157">cbdata</span><span class="sxs-lookup"><span data-stu-id="5092a-157">cbData</span></span>
  
> <span data-ttu-id="5092a-158">ULONG (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="5092a-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="5092a-159">_wzURL_ data 要素のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="5092a-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="5092a-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="5092a-160">_wzURL_</span></span>
  
> <span data-ttu-id="5092a-161">WCHAR 要素の配列。</span><span class="sxs-lookup"><span data-stu-id="5092a-161">An array of WCHAR elements.</span></span> <span data-ttu-id="5092a-162">0で終了したホームページの URL 文字列の utf-16 表現。</span><span class="sxs-lookup"><span data-stu-id="5092a-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="5092a-163">WebViewPersistenceObject Stream サンプル</span><span class="sxs-lookup"><span data-stu-id="5092a-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="5092a-164">このセクションでは、 **WebViewPersistenceObject**ストリームの例について説明します。</span><span class="sxs-lookup"><span data-stu-id="5092a-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="5092a-165">ストリームは、ホームページの URL "https://www.microsoft.com" を指定します。</span><span class="sxs-lookup"><span data-stu-id="5092a-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="5092a-166">**データダンプ**</span><span class="sxs-lookup"><span data-stu-id="5092a-166">**Data dump**</span></span>
  
<span data-ttu-id="5092a-167">次に示すのは、バイナリエディターに表示されるストリームのデータダンプです。</span><span class="sxs-lookup"><span data-stu-id="5092a-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="5092a-168">**ストリームオフセット**</span><span class="sxs-lookup"><span data-stu-id="5092a-168">**Stream offset**</span></span>|<span data-ttu-id="5092a-169">**データバイト**</span><span class="sxs-lookup"><span data-stu-id="5092a-169">**Data bytes**</span></span>|<span data-ttu-id="5092a-170">**ASCII データ**</span><span class="sxs-lookup"><span data-stu-id="5092a-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5092a-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="5092a-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="5092a-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="5092a-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="5092a-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="5092a-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="5092a-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="5092a-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="5092a-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="5092a-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="5092a-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="5092a-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="5092a-177">以下に、 **WebViewPersistenceObject**ストリームのサンプルデータの解析を示します。</span><span class="sxs-lookup"><span data-stu-id="5092a-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="5092a-178">_dwversion_</span><span class="sxs-lookup"><span data-stu-id="5092a-178">_dwVersion_</span></span>
  
> <span data-ttu-id="5092a-179">Offset 0x0、4バイト: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION)。</span><span class="sxs-lookup"><span data-stu-id="5092a-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="5092a-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="5092a-180">_dwType_</span></span>
  
> <span data-ttu-id="5092a-181">オフセット0x4、4バイト: 0x00000001 (webviewurl)。</span><span class="sxs-lookup"><span data-stu-id="5092a-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="5092a-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="5092a-182">_dwFlags_</span></span>
  
> <span data-ttu-id="5092a-183">オフセット0x8、4バイト: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT)。</span><span class="sxs-lookup"><span data-stu-id="5092a-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="5092a-184">_dwunused [7]_</span><span class="sxs-lookup"><span data-stu-id="5092a-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="5092a-185">Offset 0xC, 28 バイト: すべて0。</span><span class="sxs-lookup"><span data-stu-id="5092a-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="5092a-186">_cbdata_</span><span class="sxs-lookup"><span data-stu-id="5092a-186">_cbData_</span></span>
  
> <span data-ttu-id="5092a-187">オフセット0x28、4バイト: 0x00000032。</span><span class="sxs-lookup"><span data-stu-id="5092a-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="5092a-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="5092a-188">_wzURL_</span></span>
  
> <span data-ttu-id="5092a-189">Offset 0x2C、0x32 バイト:25 wchars の配列。</span><span class="sxs-lookup"><span data-stu-id="5092a-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="5092a-190">Unicode の0で終わる文字列値: "https://www.microsoft.com"。</span><span class="sxs-lookup"><span data-stu-id="5092a-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

