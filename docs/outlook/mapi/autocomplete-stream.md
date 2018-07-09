---
title: オートコンプリート ストリーム
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7fc1fae4ed648d59c273b20ced247f6d20e01a6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799731"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="1ed88-103">オートコンプリート ストリーム</span><span class="sxs-lookup"><span data-stu-id="1ed88-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="1ed88-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ed88-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ed88-105">Microsoft Outlook のオートコンプリートのストリームに対話する方法を知ることだけでなくもオートコンプリート ストリームのバイナリ形式を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="1ed88-106">オートコンプリートのストリームは、Microsoft Outlook 2013、Microsoft Outlook 2010、Microsoft Office Outlook 2007 では、Microsoft Outlook 2003 でのみ使用されるいくつかの管理メタデータおよびバイナリ ストリームとして保存されている受信者のプロパティの行のセットです。</span><span class="sxs-lookup"><span data-stu-id="1ed88-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="1ed88-107">メタデータはオートコンプリートのストリームに、Outlook の相互作用に関連するオートコンプリート機能が変更されたストリームを保存するときのメタデータの各ブロックではサード ・ パーティを保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="1ed88-108">つまり、サード ・ パーティはバイナリ形式の行セットの一部のみを変更し、のオートコンプリートのストリームのメタデータのブロックが既に保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="1ed88-109">ストリームのビジュアル化</span><span class="sxs-lookup"><span data-stu-id="1ed88-109">Stream Visualization</span></span>

<span data-ttu-id="1ed88-110">オートコンプリートのストリームの大まかなレイアウトは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1ed88-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="1ed88-111">メタデータ (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1ed88-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-112">メジャー バージョン番号 (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1ed88-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-113">マイナー バージョン番号 (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1ed88-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-114">行 n (4 バイト) の数</span><span class="sxs-lookup"><span data-stu-id="1ed88-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-115">(4 バイト) を 1 つの行のプロパティ p の数</span><span class="sxs-lookup"><span data-stu-id="1ed88-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-116">プロパティ タグのプロパティの 1 の (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1ed88-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-117">プロパティ 1 (4 バイト) のデータを予約</span><span class="sxs-lookup"><span data-stu-id="1ed88-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-118">プロパティの値の和集合 (8 バイト)</span><span class="sxs-lookup"><span data-stu-id="1ed88-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="1ed88-119">プロパティの値のデータ (0 または変数のバイト数)</span><span class="sxs-lookup"><span data-stu-id="1ed88-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="1ed88-120">…</span><span class="sxs-lookup"><span data-stu-id="1ed88-120"></span></span> <span data-ttu-id="1ed88-121">(P-1 のプロパティをプロパティ 2)</span><span class="sxs-lookup"><span data-stu-id="1ed88-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="1ed88-122">プロパティ タグのプロパティ p の (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1ed88-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-123">プロパティ p (4 バイト) のデータを予約します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-124">プロパティ p の値の和集合 (8 バイト)</span><span class="sxs-lookup"><span data-stu-id="1ed88-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="1ed88-125">プロパティ p の値のデータ (0 または変数のバイト数)</span><span class="sxs-lookup"><span data-stu-id="1ed88-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="1ed88-126">プロパティで [q 行 2 (4 バイト) の数</span><span class="sxs-lookup"><span data-stu-id="1ed88-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-127">…</span><span class="sxs-lookup"><span data-stu-id="1ed88-127"></span></span> <span data-ttu-id="1ed88-128">(2 つの行のプロパティ)</span><span class="sxs-lookup"><span data-stu-id="1ed88-128">(row two's properties)</span></span>
  
<span data-ttu-id="1ed88-129">…</span><span class="sxs-lookup"><span data-stu-id="1ed88-129"></span></span> <span data-ttu-id="1ed88-130">(n-1 の行を 3 行目)</span><span class="sxs-lookup"><span data-stu-id="1ed88-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="1ed88-131">プロパティの r n (4 バイト) の行の数です。</span><span class="sxs-lookup"><span data-stu-id="1ed88-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-132">…</span><span class="sxs-lookup"><span data-stu-id="1ed88-132"></span></span> <span data-ttu-id="1ed88-133">(n's の行のプロパティ)</span><span class="sxs-lookup"><span data-stu-id="1ed88-133">(row n's properties)</span></span>
  
<span data-ttu-id="1ed88-134">情報の余分なバイト数 EI (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1ed88-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="1ed88-135">余分な情報 (EI バイト)</span><span class="sxs-lookup"><span data-stu-id="1ed88-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="1ed88-136">メタデータ (8 バイト)</span><span class="sxs-lookup"><span data-stu-id="1ed88-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="1ed88-137">バイナリ構造体の例は、バイナリの例を参照してください、 [Outlook 2003/2007 NK2 ファイル形式と開発者のガイドライン](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)。</span><span class="sxs-lookup"><span data-stu-id="1ed88-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="1ed88-138">大まかなレイアウト</span><span class="sxs-lookup"><span data-stu-id="1ed88-138">High-level Layout</span></span>

<span data-ttu-id="1ed88-139">大まかに言うと、オートコンプリートのストリームのレイアウトのとおりです。</span><span class="sxs-lookup"><span data-stu-id="1ed88-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="1ed88-140">**値のデータ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-140">**Value Data**</span></span>|<span data-ttu-id="1ed88-141">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1ed88-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-142">メタデータ</span><span class="sxs-lookup"><span data-stu-id="1ed88-142">Metadata</span></span>  <br/> |<span data-ttu-id="1ed88-143">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-143">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-144">メジャー バージョン番号</span><span class="sxs-lookup"><span data-stu-id="1ed88-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="1ed88-145">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-145">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-146">マイナー バージョン番号</span><span class="sxs-lookup"><span data-stu-id="1ed88-146">Minor Version Number</span></span>  <br/> |<span data-ttu-id="1ed88-147">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-147">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-148">行セット</span><span class="sxs-lookup"><span data-stu-id="1ed88-148">Row-set</span></span>  <br/> |<span data-ttu-id="1ed88-149">可変</span><span class="sxs-lookup"><span data-stu-id="1ed88-149">Variable</span></span>  <br/> |
|<span data-ttu-id="1ed88-150">情報の余分なバイト数 EI</span><span class="sxs-lookup"><span data-stu-id="1ed88-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="1ed88-151">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-151">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-152">追加情報</span><span class="sxs-lookup"><span data-stu-id="1ed88-152">Extra information</span></span>  <br/> |<span data-ttu-id="1ed88-153">EI</span><span class="sxs-lookup"><span data-stu-id="1ed88-153">EI</span></span>  <br/> |
|<span data-ttu-id="1ed88-154">メタデータ</span><span class="sxs-lookup"><span data-stu-id="1ed88-154">Metadata</span></span>  <br/> |<span data-ttu-id="1ed88-155">8</span><span class="sxs-lookup"><span data-stu-id="1ed88-155">8</span></span>  <br/> |
   
<span data-ttu-id="1ed88-156">メジャー バージョンは 12 とは異なる場合、このストリームを読み取り、ときに、このストリームする必要がありますできません読み取りまたは書き込み。</span><span class="sxs-lookup"><span data-stu-id="1ed88-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="1ed88-157">オートコンプリートのストリームの現在のマイナー バージョンは、余分な情報のバイト カウントが 0 に設定する 0 です。</span><span class="sxs-lookup"><span data-stu-id="1ed88-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="1ed88-158">マイナー バージョンが 0 以外の場合は、ストリームを読み取るときに読み取りおよびストリームを作成するときに保持する必要がある余分な情報の情報があります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="1ed88-159">マイナー バージョンのストリームを作成するときに保持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="1ed88-160">これらの両方は保持されません、追加情報を記述した Outlook のインスタンスでデータが失われます。</span><span class="sxs-lookup"><span data-stu-id="1ed88-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1ed88-161">アプリケーションは、追加の情報フィールドにカスタム データを追加や形式に、Outlook の拡張機能していない任意のサードパーティの拡張機能をサポートするためには、この機能には、マイナー バージョンを変更する必要がありますいません。</span><span class="sxs-lookup"><span data-stu-id="1ed88-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="1ed88-162">行セットのレイアウト</span><span class="sxs-lookup"><span data-stu-id="1ed88-162">Row-set Layout</span></span>

<span data-ttu-id="1ed88-163">行セットのレイアウトは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1ed88-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="1ed88-164">**値のデータ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-164">**Value Data**</span></span>|<span data-ttu-id="1ed88-165">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1ed88-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-166">行数</span><span class="sxs-lookup"><span data-stu-id="1ed88-166">Number of rows</span></span>  <br/> |<span data-ttu-id="1ed88-167">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-167">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-168">Rows</span><span class="sxs-lookup"><span data-stu-id="1ed88-168">Rows</span></span>  <br/> |<span data-ttu-id="1ed88-169">可変</span><span class="sxs-lookup"><span data-stu-id="1ed88-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="1ed88-170">行の数は、行の数には、バイナリ ストリーム シーケンスの次の部分を識別します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="1ed88-171">行レイアウト</span><span class="sxs-lookup"><span data-stu-id="1ed88-171">Row Layout</span></span>

<span data-ttu-id="1ed88-172">各行は、次の形式のです。</span><span class="sxs-lookup"><span data-stu-id="1ed88-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="1ed88-173">**値のデータ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-173">**Value Data**</span></span>|<span data-ttu-id="1ed88-174">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1ed88-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-175">プロパティの数</span><span class="sxs-lookup"><span data-stu-id="1ed88-175">Number of properties</span></span>  <br/> |<span data-ttu-id="1ed88-176">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-176">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-177">プロパティ</span><span class="sxs-lookup"><span data-stu-id="1ed88-177">Properties</span></span>  <br/> |<span data-ttu-id="1ed88-178">可変</span><span class="sxs-lookup"><span data-stu-id="1ed88-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="1ed88-179">プロパティの数は、数のプロパティには、バイナリ ストリーム シーケンスの次の部分を識別します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="1ed88-180">プロパティのレイアウト</span><span class="sxs-lookup"><span data-stu-id="1ed88-180">Property Layout</span></span>

<span data-ttu-id="1ed88-181">各プロパティは、次の形式のです。</span><span class="sxs-lookup"><span data-stu-id="1ed88-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="1ed88-182">**値のデータ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-182">**Value Data**</span></span>|<span data-ttu-id="1ed88-183">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1ed88-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-184">プロパティ タグ</span><span class="sxs-lookup"><span data-stu-id="1ed88-184">Property Tag</span></span>  <br/> |<span data-ttu-id="1ed88-185">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-185">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-186">予約済みのデータ</span><span class="sxs-lookup"><span data-stu-id="1ed88-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="1ed88-187">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-187">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-188">プロパティの値の和集合</span><span class="sxs-lookup"><span data-stu-id="1ed88-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="1ed88-189">値のデータ</span><span class="sxs-lookup"><span data-stu-id="1ed88-189">Value Data</span></span>  <br/> |<span data-ttu-id="1ed88-190">0 または変数 (prop タグによって)</span><span class="sxs-lookup"><span data-stu-id="1ed88-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="1ed88-191">プロパティの値を解釈します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-191">Interpreting the Property Value</span></span>

<span data-ttu-id="1ed88-192">プロパティ値ユニオンと値のデータは、プロパティ ブロックの最初の 4 バイトのプロパティ タグに基づいて解釈されます。</span><span class="sxs-lookup"><span data-stu-id="1ed88-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="1ed88-193">このプロパティ タグは、MAPI プロパティ タグと同じ形式にします。</span><span class="sxs-lookup"><span data-stu-id="1ed88-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="1ed88-194">ビット 0 ~ 15 のプロパティ タグは、プロパティの種類です。</span><span class="sxs-lookup"><span data-stu-id="1ed88-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="1ed88-195">31 までの 16 ビットとは、プロパティの識別子です。</span><span class="sxs-lookup"><span data-stu-id="1ed88-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="1ed88-196">プロパティの型は、プロパティの残りの部分を読み取る必要がある方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="1ed88-197">静的な値</span><span class="sxs-lookup"><span data-stu-id="1ed88-197">Static Value</span></span>

<span data-ttu-id="1ed88-198">いくつかのプロパティは、値のデータが含まれていないとだけ、共用体のデータがあります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="1ed88-199">(プロパティ タグからのもの) を次のプロパティの種類は、次のように 8 バイトのプロパティの共用体のデータを扱う必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="1ed88-200">**プロペラの種類**</span><span class="sxs-lookup"><span data-stu-id="1ed88-200">**Prop Type**</span></span>|<span data-ttu-id="1ed88-201">**プロパティの共用体の解釈**</span><span class="sxs-lookup"><span data-stu-id="1ed88-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="1ed88-202">PT_I2</span></span>  <br/> |<span data-ttu-id="1ed88-203">短い int</span><span class="sxs-lookup"><span data-stu-id="1ed88-203">short int</span></span>  <br/> |
|<span data-ttu-id="1ed88-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1ed88-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="1ed88-205">long</span><span class="sxs-lookup"><span data-stu-id="1ed88-205">long</span></span>  <br/> |
|<span data-ttu-id="1ed88-206">PT_R4</span><span class="sxs-lookup"><span data-stu-id="1ed88-206">PT_R4</span></span>  <br/> |<span data-ttu-id="1ed88-207">浮動小数点数</span><span class="sxs-lookup"><span data-stu-id="1ed88-207">float</span></span>  <br/> |
|<span data-ttu-id="1ed88-208">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="1ed88-208">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="1ed88-209">double</span><span class="sxs-lookup"><span data-stu-id="1ed88-209">double</span></span>  <br/> |
|<span data-ttu-id="1ed88-210">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1ed88-210">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="1ed88-211">短い int</span><span class="sxs-lookup"><span data-stu-id="1ed88-211">short int</span></span>  <br/> |
|<span data-ttu-id="1ed88-212">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1ed88-212">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="1ed88-213">FILETIME</span><span class="sxs-lookup"><span data-stu-id="1ed88-213">FILETIME</span></span>  <br/> |
|<span data-ttu-id="1ed88-214">PT_I8</span><span class="sxs-lookup"><span data-stu-id="1ed88-214">PT_I8</span></span>  <br/> |<span data-ttu-id="1ed88-215">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="1ed88-215">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="1ed88-216">動的な値</span><span class="sxs-lookup"><span data-stu-id="1ed88-216">Dynamic Values</span></span>

<span data-ttu-id="1ed88-217">プロパティ タグ、予約済みのデータでは、およびそのプロパティ値共用体に含まれる最初の 16 バイトの後の他のプロパティ値のデータ ブロックのデータであります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-217">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="1ed88-218">静的な値とは異なりは、8 バイトのプロパティの値の共用体に格納されているデータは読み取りに関連するではありません。</span><span class="sxs-lookup"><span data-stu-id="1ed88-218">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="1ed88-219">記述する場合は、値を使用して、これらの 8 バイトを入力することを確認します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-219">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="1ed88-220">ただし、8 バイトの内容は重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="1ed88-220">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="1ed88-221">動的な値では、プロパティ タグの種類は、値のデータを解釈する方法を決定します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-221">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="1ed88-222">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="1ed88-222">PT_STRING8</span></span> 
  
|<span data-ttu-id="1ed88-223">**値のデータ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-223">**Value Data**</span></span>|<span data-ttu-id="1ed88-224">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1ed88-224">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-225">バイト n の数</span><span class="sxs-lookup"><span data-stu-id="1ed88-225">Number of bytes n</span></span>  <br/> |<span data-ttu-id="1ed88-226">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-226">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-227">ANSI 文字列 (終端の NULL 文字が含まれています) として解釈されるバイト数</span><span class="sxs-lookup"><span data-stu-id="1ed88-227">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="1ed88-228">n</span><span class="sxs-lookup"><span data-stu-id="1ed88-228">n</span></span>  <br/> |
   
<span data-ttu-id="1ed88-229">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="1ed88-229">PT_CLSID</span></span>
  
|<span data-ttu-id="1ed88-230">**値のデータ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-230">**Value Data**</span></span>|<span data-ttu-id="1ed88-231">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1ed88-231">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-232">GUID として解釈されるバイト数</span><span class="sxs-lookup"><span data-stu-id="1ed88-232">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="1ed88-233">16</span><span class="sxs-lookup"><span data-stu-id="1ed88-233">16</span></span>  <br/> |
|||
   
<span data-ttu-id="1ed88-234">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ed88-234">PT_BINARY</span></span> 
  
|<span data-ttu-id="1ed88-235">**値のデータ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-235">**Value Data**</span></span>|<span data-ttu-id="1ed88-236">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1ed88-236">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-237">バイト n の数</span><span class="sxs-lookup"><span data-stu-id="1ed88-237">Number of bytes n</span></span>  <br/> |<span data-ttu-id="1ed88-238">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-238">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-239">バイトをバイト配列として解釈されるように</span><span class="sxs-lookup"><span data-stu-id="1ed88-239">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="1ed88-240">n</span><span class="sxs-lookup"><span data-stu-id="1ed88-240">n</span></span>  <br/> |
   
<span data-ttu-id="1ed88-241">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="1ed88-241">PT_ERROR</span></span>
  
|<span data-ttu-id="1ed88-242">**値のデータ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-242">**Value Data**</span></span>|<span data-ttu-id="1ed88-243">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1ed88-243">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-244">バイト n の数</span><span class="sxs-lookup"><span data-stu-id="1ed88-244">Number of bytes n</span></span>  <br/> |<span data-ttu-id="1ed88-245">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-245">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-246">バイトをバイト配列として解釈されるように</span><span class="sxs-lookup"><span data-stu-id="1ed88-246">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="1ed88-247">n</span><span class="sxs-lookup"><span data-stu-id="1ed88-247">n</span></span>  <br/> |
   
<span data-ttu-id="1ed88-248">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="1ed88-248">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="1ed88-249">**値のデータ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-249">**Value Data**</span></span>|<span data-ttu-id="1ed88-250">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1ed88-250">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-251">バイナリ配列 X の数</span><span class="sxs-lookup"><span data-stu-id="1ed88-251">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="1ed88-252">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-252">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-253">A が X を含むバイトの実行バイナリ配列です。</span><span class="sxs-lookup"><span data-stu-id="1ed88-253">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="1ed88-254">各配列は、実行 PT_BINARY バイトと同じように解釈する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-254">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="1ed88-255">可変</span><span class="sxs-lookup"><span data-stu-id="1ed88-255">Variable</span></span>  <br/> |
   
<span data-ttu-id="1ed88-256">PT_MV_STRING8 (Outlook 2007、Outlook 2010、Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="1ed88-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="1ed88-257">**値のデータ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-257">**Value Data**</span></span>|<span data-ttu-id="1ed88-258">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1ed88-258">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-259">ANSI 文字列 X の数</span><span class="sxs-lookup"><span data-stu-id="1ed88-259">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="1ed88-260">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-260">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-261">X の ANSI 文字列を含むバイトの実行します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-261">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="1ed88-262">実行 PT_STRING8 バイトと同じように各文字列を解釈する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-262">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="1ed88-263">可変</span><span class="sxs-lookup"><span data-stu-id="1ed88-263">Variable</span></span>  <br/> |
   
<span data-ttu-id="1ed88-264">PT_MV_UNICODE (Outlook 2007、Outlook 2010、Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="1ed88-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="1ed88-265">**値のデータ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-265">**Value Data**</span></span>|<span data-ttu-id="1ed88-266">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1ed88-266">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1ed88-267">UNICODE 文字列 X の数</span><span class="sxs-lookup"><span data-stu-id="1ed88-267">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="1ed88-268">4</span><span class="sxs-lookup"><span data-stu-id="1ed88-268">4</span></span>  <br/> |
|<span data-ttu-id="1ed88-269">X UNICODE の文字列が格納されたバイトの実行します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-269">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="1ed88-270">実行 PT_UNICODE バイトと同じように各文字列を解釈する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-270">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="1ed88-271">可変</span><span class="sxs-lookup"><span data-stu-id="1ed88-271">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="1ed88-272">重要なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1ed88-272">Significant properties</span></span>

<span data-ttu-id="1ed88-273">このトピックで述べたように、アドレス帳の受信者のプロパティに対応するプロパティ タグがあるプロパティを表すバイナリのブロックです。</span><span class="sxs-lookup"><span data-stu-id="1ed88-273">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="1ed88-274">プロパティの説明を検索するには、ここに示されていないプロパティの場合は、 http://msdn.microsoft.com/ja-jp/library/cc433490(EXCHG.80).aspx。</span><span class="sxs-lookup"><span data-stu-id="1ed88-274">For properties that are not listed here, you can look up the property description at http://msdn.microsoft.com/ja-jp/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="1ed88-275">**プロパティ名**</span><span class="sxs-lookup"><span data-stu-id="1ed88-275">**Property Name**</span></span>|<span data-ttu-id="1ed88-276">**プロパティ タグ**</span><span class="sxs-lookup"><span data-stu-id="1ed88-276">**Property Tag**</span></span>|<span data-ttu-id="1ed88-277">**説明 (詳細については MSDN を参照してください)**</span><span class="sxs-lookup"><span data-stu-id="1ed88-277">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ed88-278">(オートコンプリートのストリームのみを特定の受信者には送信されません) PR_NICK_NAME_W</span><span class="sxs-lookup"><span data-stu-id="1ed88-278">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="1ed88-279">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="1ed88-279">0x6001001f</span></span>  <br/> |<span data-ttu-id="1ed88-280">このプロパティは、受信者の各行の先頭である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-280">This property must be first in each recipient row.</span></span> <span data-ttu-id="1ed88-281">機能的には受信者の行のキーの識別子として機能します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-281">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="1ed88-282">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1ed88-282">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="1ed88-283">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="1ed88-283">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="1ed88-284">受信者のアドレス帳エントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="1ed88-284">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="1ed88-285">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="1ed88-285">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="1ed88-286">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="1ed88-286">0x3001001F</span></span>  <br/> |<span data-ttu-id="1ed88-287">受信者の表示名です。</span><span class="sxs-lookup"><span data-stu-id="1ed88-287">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="1ed88-288">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="1ed88-288">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="1ed88-289">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="1ed88-289">0x3003001F</span></span>  <br/> |<span data-ttu-id="1ed88-290">受信者の電子メール アドレス (johndoe@contoso.com または/o など = Contoso と OU = Foo と cn = 受信者と cn = johndoe)</span><span class="sxs-lookup"><span data-stu-id="1ed88-290">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="1ed88-291">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="1ed88-291">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="1ed88-292">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="1ed88-292">0x3002001F</span></span>  <br/> |<span data-ttu-id="1ed88-293">受信者のアドレスの種類 (SMTP または EX など)。</span><span class="sxs-lookup"><span data-stu-id="1ed88-293">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="1ed88-294">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="1ed88-294">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="1ed88-295">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="1ed88-295">0x300B0102</span></span>  <br/> |<span data-ttu-id="1ed88-296">受信者の MAPI 検索キーです。</span><span class="sxs-lookup"><span data-stu-id="1ed88-296">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="1ed88-297">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="1ed88-297">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="1ed88-298">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="1ed88-298">0x39FE001f</span></span>  <br/> |<span data-ttu-id="1ed88-299">受信者の SMTP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="1ed88-299">The recipient's SMTP address.</span></span>  <br/> |
|<span data-ttu-id="1ed88-300">(オートコンプリートのストリームのみを特定の受信者には送信されません) PR_DROPDOWN_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="1ed88-300">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="1ed88-301">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="1ed88-301">0X6003001f</span></span>  <br/> |<span data-ttu-id="1ed88-302">オートコンプリートの候補一覧に表示される表示文字列。</span><span class="sxs-lookup"><span data-stu-id="1ed88-302">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="1ed88-303">(オートコンプリートのストリームのみを特定の受信者には送信されません) PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="1ed88-303">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="1ed88-304">0x60040003</span><span class="sxs-lookup"><span data-stu-id="1ed88-304">0x60040003</span></span>  <br/> |<span data-ttu-id="1ed88-305">このオートコンプリート エントリの重量。</span><span class="sxs-lookup"><span data-stu-id="1ed88-305">The weight of this autocomplete entry.</span></span> <span data-ttu-id="1ed88-306">重量を使用すると、オートコンプリートの候補一覧を照合するときにどのような順序のオートコンプリート エントリが発生するを決定します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-306">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="1ed88-307">下の重みを持つエントリの前より高い負荷を持つエントリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1ed88-307">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="1ed88-308">完全なオートコンプリート リストは、このプロパティによって並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="1ed88-308">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="1ed88-309">重量は定期的に時間の経過と共に減少し、ユーザーは、この受信者に電子メールを送信すると大ききます。</span><span class="sxs-lookup"><span data-stu-id="1ed88-309">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="1ed88-310">このプロパティの詳細についてはこのトピックの後半の説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ed88-310">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="1ed88-311">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="1ed88-311">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="1ed88-312">オートコンプリートのストリーム内の行のセットが PR_NICK_NAME_WEIGHT プロパティによって降順にソートし、オートコンプリートのストリームは、この並べ替えられた特性に常に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ed88-312">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="1ed88-313">したがって、行の幅への変更も確認してくださいの行の位置が、完全な行セットの並べ替え順を維持します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-313">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="1ed88-314">並べ替えの順序を維持するために適切な位置に挿入する行セットに追加します。</span><span class="sxs-lookup"><span data-stu-id="1ed88-314">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="1ed88-315">この重量の最小値は 0x1 で、最大値は LONG_MAX です。</span><span class="sxs-lookup"><span data-stu-id="1ed88-315">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="1ed88-316">重量の他の値は、無効と見なされます。</span><span class="sxs-lookup"><span data-stu-id="1ed88-316">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="1ed88-317">ときにメールを送信する Outlook 2007 上げたり、受信者を解決するにはその受信者の重量 0x2000 で。</span><span class="sxs-lookup"><span data-stu-id="1ed88-317">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

