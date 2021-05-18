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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316311"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="0becd-103">PidTagFolderWebViewInfo 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="0becd-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="0becd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0becd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0becd-105">Microsoft のフォルダーのホーム ページの URL が含Outlook。</span><span class="sxs-lookup"><span data-stu-id="0becd-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="0becd-106">このプロパティには **、WebViewPersistenceObject というバイナリ ストリームが含まれます**。</span><span class="sxs-lookup"><span data-stu-id="0becd-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0becd-107">関連するプロパティ:</span><span class="sxs-lookup"><span data-stu-id="0becd-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="0becd-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="0becd-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="0becd-109">識別子:</span><span class="sxs-lookup"><span data-stu-id="0becd-109">Identifier:</span></span>  <br/> |<span data-ttu-id="0becd-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="0becd-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="0becd-111">データの種類 : </span><span class="sxs-lookup"><span data-stu-id="0becd-111">Data type:</span></span>  <br/> |<span data-ttu-id="0becd-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0becd-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0becd-113">エリア:</span><span class="sxs-lookup"><span data-stu-id="0becd-113">Area:</span></span>  <br/> |<span data-ttu-id="0becd-114">MAPI フォルダー</span><span class="sxs-lookup"><span data-stu-id="0becd-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0becd-115">注釈</span><span class="sxs-lookup"><span data-stu-id="0becd-115">Remarks</span></span>

<span data-ttu-id="0becd-116">ホーム ページの URL は、任意のフォルダーにOutlookできます。</span><span class="sxs-lookup"><span data-stu-id="0becd-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="0becd-117">この情報は、フォルダー Outlook [プロパティ] ダイアログ ボックスの **[** ホーム ページ] タブからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="0becd-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="0becd-118">特定のポリシー設定によっては、このフォルダーを含む MAPI ストアが[IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md)実装で MSCAP_SECURE_FOLDER_HOMEPAGES を報告しない場合、ホーム ページは Outlook によって無視される場合があります。</span><span class="sxs-lookup"><span data-stu-id="0becd-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="0becd-119">[今日 **Outlook]フォルダー** とパブリック フォルダーの両方に、ホーム ページの URL を設定できます。</span><span class="sxs-lookup"><span data-stu-id="0becd-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="0becd-120">ただし **、Outlook Today** フォルダーは、別のメカニズムを使用してホーム ページの URL を管理します。このメカニズムについては、このトピックでは説明しない。</span><span class="sxs-lookup"><span data-stu-id="0becd-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="0becd-121">パブリック フォルダーには、ユーザーに固有のホーム ページ URL が定義されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="0becd-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="0becd-122">ただし、この機能については、このトピックでは説明していない。</span><span class="sxs-lookup"><span data-stu-id="0becd-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="0becd-123">このプロパティの値は **、WebViewPersistenceObject というバイナリ ストリームです**。</span><span class="sxs-lookup"><span data-stu-id="0becd-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="0becd-124">WebViewPersistenceObject ストリーム構造</span><span class="sxs-lookup"><span data-stu-id="0becd-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="0becd-125">**WebViewPersistenceObject ストリーム** 構造には、フォルダーのホーム ページ URL に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0becd-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="0becd-126">この構造体のデータ要素は、次の指定された順序で、お客様の直後に、リトル エンドのバイト順に格納されます。</span><span class="sxs-lookup"><span data-stu-id="0becd-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0becd-127">次の説明では、ユーザーがサポートするフィールド値の一覧Outlook。したがって、コードが既存のストリームを読み取る場合、ここにリストされていないフラグも見つかる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0becd-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="0becd-128">ただし、この説明を使用すると、プログラムで理解できる **PidTagFolderWebViewInfo** プロパティOutlook作成できます。</span><span class="sxs-lookup"><span data-stu-id="0becd-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="0becd-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="0becd-129">_dwVersion_</span></span>
  
> <span data-ttu-id="0becd-130">DWORD (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="0becd-130">DWORD (4 bytes).</span></span> <span data-ttu-id="0becd-131">構造の形式のバージョン。</span><span class="sxs-lookup"><span data-stu-id="0becd-131">The version of the structure's format.</span></span> <span data-ttu-id="0becd-132">2007 Microsoft Office Outlook現在、このフィールドでサポートされている唯一の値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0becd-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="0becd-133">**値の名前**</span><span class="sxs-lookup"><span data-stu-id="0becd-133">**Value name**</span></span>|<span data-ttu-id="0becd-134">**値**</span><span class="sxs-lookup"><span data-stu-id="0becd-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0becd-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="0becd-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="0becd-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="0becd-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="0becd-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="0becd-137">_dwType_</span></span>
  
> <span data-ttu-id="0becd-138">DWORD (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="0becd-138">DWORD (4 bytes).</span></span> <span data-ttu-id="0becd-139">ホーム ページ情報の種類。</span><span class="sxs-lookup"><span data-stu-id="0becd-139">The type of the home page information.</span></span> <span data-ttu-id="0becd-140">2007 Microsoft Office Outlook現在、このフィールドでサポートされている唯一の値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="0becd-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="0becd-141">**値の名前**</span><span class="sxs-lookup"><span data-stu-id="0becd-141">**Value name**</span></span>|<span data-ttu-id="0becd-142">**値**</span><span class="sxs-lookup"><span data-stu-id="0becd-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0becd-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="0becd-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="0becd-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0becd-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="0becd-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="0becd-145">_dwFlags_</span></span>
  
> <span data-ttu-id="0becd-146">DWORD (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="0becd-146">DWORD (4 bytes).</span></span> <span data-ttu-id="0becd-147">次の表に、値と意味を持つ 0 個以上のフラグの組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="0becd-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="0becd-148">フラグ名\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0becd-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="0becd-149">\*\*\*\*値\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0becd-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="0becd-150">\*\*\*\*説明\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="0becd-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0becd-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="0becd-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="0becd-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="0becd-152">0x00000001</span></span>  <br/> |<span data-ttu-id="0becd-153">[**このフォルダーのホーム ページ** を既定で表示する] チェックボックスは、フォルダーの [プロパティ] ダイアログ ボックスの [ホーム ページ] タブでオンになっています。</span><span class="sxs-lookup"><span data-stu-id="0becd-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="0becd-154">_dwUnused[7]_</span><span class="sxs-lookup"><span data-stu-id="0becd-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="0becd-155">7 DWORD 要素の配列 (合計 28 バイト)。</span><span class="sxs-lookup"><span data-stu-id="0becd-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="0becd-156">未使用。</span><span class="sxs-lookup"><span data-stu-id="0becd-156">Unused.</span></span>
    
<span data-ttu-id="0becd-157">cbData</span><span class="sxs-lookup"><span data-stu-id="0becd-157">cbData</span></span>
  
> <span data-ttu-id="0becd-158">ULONG (4 バイト)。</span><span class="sxs-lookup"><span data-stu-id="0becd-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="0becd-159">_wzURL_ データ要素のサイズ (バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="0becd-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="0becd-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="0becd-160">_wzURL_</span></span>
  
> <span data-ttu-id="0becd-161">WCHAR 要素の配列。</span><span class="sxs-lookup"><span data-stu-id="0becd-161">An array of WCHAR elements.</span></span> <span data-ttu-id="0becd-162">終了ゼロのホーム ページ URL 文字列の UTF-16 表記。</span><span class="sxs-lookup"><span data-stu-id="0becd-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="0becd-163">WebViewPersistenceObject ストリームのサンプル</span><span class="sxs-lookup"><span data-stu-id="0becd-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="0becd-164">このセクションでは **、WebViewPersistenceObject ストリームの例について説明** します。</span><span class="sxs-lookup"><span data-stu-id="0becd-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="0becd-165">ストリームは、ホーム ページの URL " を指定 https://www.microsoft.com します。</span><span class="sxs-lookup"><span data-stu-id="0becd-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="0becd-166">**データ ダンプ**</span><span class="sxs-lookup"><span data-stu-id="0becd-166">**Data dump**</span></span>
  
<span data-ttu-id="0becd-167">バイナリ エディターに表示されるストリームのデータ ダンプを次に示します。</span><span class="sxs-lookup"><span data-stu-id="0becd-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="0becd-168">**ストリーム のオフセット**</span><span class="sxs-lookup"><span data-stu-id="0becd-168">**Stream offset**</span></span>|<span data-ttu-id="0becd-169">**データ バイト**</span><span class="sxs-lookup"><span data-stu-id="0becd-169">**Data bytes**</span></span>|<span data-ttu-id="0becd-170">**ASCII データ**</span><span class="sxs-lookup"><span data-stu-id="0becd-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0becd-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="0becd-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="0becd-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="0becd-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="0becd-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="0becd-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="0becd-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="0becd-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="0becd-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="0becd-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="0becd-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="0becd-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="0becd-177">**WebViewPersistenceObject** ストリームのサンプル データの解析を次に示します。</span><span class="sxs-lookup"><span data-stu-id="0becd-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="0becd-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="0becd-178">_dwVersion_</span></span>
  
> <span data-ttu-id="0becd-179">オフセット0x0 4 バイト: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION)。</span><span class="sxs-lookup"><span data-stu-id="0becd-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="0becd-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="0becd-180">_dwType_</span></span>
  
> <span data-ttu-id="0becd-181">オフセット0x4 4 バイト: 0x00000001 (WEBVIEWURL)。</span><span class="sxs-lookup"><span data-stu-id="0becd-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="0becd-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="0becd-182">_dwFlags_</span></span>
  
> <span data-ttu-id="0becd-183">オフセット0x8 4 バイト: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT)。</span><span class="sxs-lookup"><span data-stu-id="0becd-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="0becd-184">_dwUnused[7]_</span><span class="sxs-lookup"><span data-stu-id="0becd-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="0becd-185">オフセット0xC 28 バイト: すべてのゼロ。</span><span class="sxs-lookup"><span data-stu-id="0becd-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="0becd-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="0becd-186">_cbData_</span></span>
  
> <span data-ttu-id="0becd-187">オフセット0x28、4 バイト: 0x00000032。</span><span class="sxs-lookup"><span data-stu-id="0becd-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="0becd-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="0becd-188">_wzURL_</span></span>
  
> <span data-ttu-id="0becd-189">オフセット0x2C、0x32バイト: 25 WCHARs の配列。</span><span class="sxs-lookup"><span data-stu-id="0becd-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="0becd-190">Unicode のゼロ終端文字列値: " https://www.microsoft.com ".</span><span class="sxs-lookup"><span data-stu-id="0becd-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

