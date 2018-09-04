---
title: オートコンプリート ストリーム
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: caa93fcc1675531f2d128170c81904e0e286e0f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591080"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="1f14c-103">オートコンプリート ストリーム</span><span class="sxs-lookup"><span data-stu-id="1f14c-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="1f14c-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f14c-104">**Applies to:** Office 365 | Outlook | Outlook 2016 \*</span></span> 
  
<span data-ttu-id="1f14c-105">Microsoft Outlook とオートコンプリート ストリームの相互作用の仕組みを知ることはもちろん重要ですが、オートコンプリート ストリームのバイナリ形式も理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="1f14c-106">オートコンプリート ストリームは、Microsoft Outlook 2013、Microsoft Outlook 2010、Microsoft Office Outlook 2007、Microsoft Outlook 2003 のみで使用される一部のブックキーピングのメタデータと一緒にバイナリ ストリームとして保存される受信者プロパティの行の一式です。</span><span class="sxs-lookup"><span data-stu-id="1f14c-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="1f14c-107">メタデータは Outlook とオートコンプリート ストリームの相互作用に関連します。そのため、サード パーティは、オートコンプリート ストリームの変更を保存する場合、メアデータのブロックごとの内容をそのままにしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="1f14c-108">つまり、サード パーティはバイナリ形式の行セットの部分のみを変更して、オートコンプリート ストリームのメタデータのブロックの内容はそのままにします。</span><span class="sxs-lookup"><span data-stu-id="1f14c-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="1f14c-109">ストリームの視覚化</span><span class="sxs-lookup"><span data-stu-id="1f14c-109">Stream Visualization</span></span>

<span data-ttu-id="1f14c-110">以下が、オートコンプリート ストリームのレイアウトの概要になります:</span><span class="sxs-lookup"><span data-stu-id="1f14c-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="1f14c-111">メタデータ (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-112">メジャー バージョン番号 (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-113">マイナー バージョン番号 (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-114">行 n の数 (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-115">行 1 のプロパティ p の数 (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-116">プロパティ 1 のプロパティ タグ (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-117">プロパティ 1 の予約済みのデータ (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-118">プロパティ 1 の値の和集合 (8 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="1f14c-119">プロパティ 1 の値のデータ (0 または変数バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="1f14c-120">…</span><span class="sxs-lookup"><span data-stu-id="1f14c-120"></span></span> <span data-ttu-id="1f14c-121">(プロパティ P-1 を介したプロパティ 2)</span><span class="sxs-lookup"><span data-stu-id="1f14c-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="1f14c-122">プロパティ p のプロパティ タグ (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-123">プロパティ p の予約済みのデータ (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-124">プロパティ p の値の和集合 (8 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="1f14c-125">プロパティ p の値のデータ (0 または変数バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="1f14c-126">行 2 のプロパティ q の数 (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-127">…</span><span class="sxs-lookup"><span data-stu-id="1f14c-127"></span></span> <span data-ttu-id="1f14c-128">(行 2 のプロパティ)</span><span class="sxs-lookup"><span data-stu-id="1f14c-128">(row two's properties)</span></span>
  
<span data-ttu-id="1f14c-129">…</span><span class="sxs-lookup"><span data-stu-id="1f14c-129"></span></span> <span data-ttu-id="1f14c-130">(行 n-1 を介した行 3)</span><span class="sxs-lookup"><span data-stu-id="1f14c-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="1f14c-131">行 n のプロパティ r の数 (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-132">…</span><span class="sxs-lookup"><span data-stu-id="1f14c-132"></span></span> <span data-ttu-id="1f14c-133">(行 n のプロパティ)</span><span class="sxs-lookup"><span data-stu-id="1f14c-133">(row n's properties)</span></span>
  
<span data-ttu-id="1f14c-134">追加情報のバイト数 EI (4 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="1f14c-135">追加情報 (EI バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="1f14c-136">メタデータ (8 バイト)</span><span class="sxs-lookup"><span data-stu-id="1f14c-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="1f14c-137">バイナリ構造の例に関しては、「[Outlook 2003/2007 NK2 のファイル形式と開発者向けガイドライン](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)」にあるバイナリの例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1f14c-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="1f14c-138">レイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="1f14c-138">High-level Layout</span></span>

<span data-ttu-id="1f14c-139">以下が、オートコンプリート ストリームのレイアウトの概要になります:</span><span class="sxs-lookup"><span data-stu-id="1f14c-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="1f14c-140">**値データ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-140">**Value Data**</span></span>|<span data-ttu-id="1f14c-141">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1f14c-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-142">Metadata</span><span class="sxs-lookup"><span data-stu-id="1f14c-142">Metadata</span></span>  <br/> |<span data-ttu-id="1f14c-143">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-143">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-144">メジャー バージョン番号</span><span class="sxs-lookup"><span data-stu-id="1f14c-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="1f14c-145">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-145">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-146">マイナー バージョン番号</span><span class="sxs-lookup"><span data-stu-id="1f14c-146">Minor version number</span></span>  <br/> |<span data-ttu-id="1f14c-147">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-147">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-148">行セット</span><span class="sxs-lookup"><span data-stu-id="1f14c-148">rowset</span></span>  <br/> |<span data-ttu-id="1f14c-149">変数</span><span class="sxs-lookup"><span data-stu-id="1f14c-149">Variable</span></span>  <br/> |
|<span data-ttu-id="1f14c-150">追加情報のバイト数 EI</span><span class="sxs-lookup"><span data-stu-id="1f14c-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="1f14c-151">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-151">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-152">追加情報</span><span class="sxs-lookup"><span data-stu-id="1f14c-152">Extra information</span></span>  <br/> |<span data-ttu-id="1f14c-153">EI</span><span class="sxs-lookup"><span data-stu-id="1f14c-153">E-I</span></span>  <br/> |
|<span data-ttu-id="1f14c-154">Metadata</span><span class="sxs-lookup"><span data-stu-id="1f14c-154">Metadata</span></span>  <br/> |<span data-ttu-id="1f14c-155">8</span><span class="sxs-lookup"><span data-stu-id="1f14c-155">-8</span></span>  <br/> |
   
<span data-ttu-id="1f14c-156">このストリームを読み取るときのメジャー バージョンが 12 でない場合は、ストリームの読み取りまたは書き込みは行われません。</span><span class="sxs-lookup"><span data-stu-id="1f14c-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="1f14c-157">現行のオートコンプリート ストリームのマイナー バージョンは 0 で、追加情報のバイト数は 0 に設定されています。</span><span class="sxs-lookup"><span data-stu-id="1f14c-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="1f14c-158">マイナー バージョンが 0 でない場合は、追加情報内に、ストリームの読み取り時に読み取る情報とストリームの書き込み時に内容を保持する情報が格納されます。</span><span class="sxs-lookup"><span data-stu-id="1f14c-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="1f14c-159">ストリームを書き込むときには、マイナー バージョンもそのままにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="1f14c-160">これら両方の内容が維持されていないと、追加情報を書き込んだ Outlook のインスタンスはデータを失います。</span><span class="sxs-lookup"><span data-stu-id="1f14c-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1f14c-161">アプリケーションで、カスタム データを追加情報のフィールドへ追加したり、マイナー バージョンを変更したりすることはできません。この機能は、Outlook の拡張機能の形式に対してサポートされており、任意のサードパーティの拡張機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="1f14c-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="1f14c-162">行セットのレイアウト</span><span class="sxs-lookup"><span data-stu-id="1f14c-162">Row-set Layout</span></span>

<span data-ttu-id="1f14c-163">行セットのレイアウトは次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="1f14c-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="1f14c-164">**値データ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-164">**Value Data**</span></span>|<span data-ttu-id="1f14c-165">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1f14c-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-166">行数</span><span class="sxs-lookup"><span data-stu-id="1f14c-166">Number of rows</span></span>  <br/> |<span data-ttu-id="1f14c-167">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-167">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-168">行</span><span class="sxs-lookup"><span data-stu-id="1f14c-168">Rows</span></span>  <br/> |<span data-ttu-id="1f14c-169">変数</span><span class="sxs-lookup"><span data-stu-id="1f14c-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="1f14c-170">行数は、バイナリ ストリーム シーケンスの次の部分の行数を示します。</span><span class="sxs-lookup"><span data-stu-id="1f14c-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="1f14c-171">行のレイアウト</span><span class="sxs-lookup"><span data-stu-id="1f14c-171">Row Layout</span></span>

<span data-ttu-id="1f14c-172">それぞれの行は、次の形式になります:</span><span class="sxs-lookup"><span data-stu-id="1f14c-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="1f14c-173">**値データ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-173">**Value Data**</span></span>|<span data-ttu-id="1f14c-174">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1f14c-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-175">プロパティ数</span><span class="sxs-lookup"><span data-stu-id="1f14c-175">Number of properties</span></span>  <br/> |<span data-ttu-id="1f14c-176">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-176">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-177">プロパティ</span><span class="sxs-lookup"><span data-stu-id="1f14c-177">Properties</span></span>  <br/> |<span data-ttu-id="1f14c-178">変数</span><span class="sxs-lookup"><span data-stu-id="1f14c-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="1f14c-179">プロパティ数は、バイナリ ストリーム シーケンスの次の部分のプロパティ数を示します。</span><span class="sxs-lookup"><span data-stu-id="1f14c-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="1f14c-180">プロパティのレイアウト</span><span class="sxs-lookup"><span data-stu-id="1f14c-180">Layout Property</span></span>

<span data-ttu-id="1f14c-181">それぞれのプロパティは、次の形式になります:</span><span class="sxs-lookup"><span data-stu-id="1f14c-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="1f14c-182">**値データ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-182">**Value Data**</span></span>|<span data-ttu-id="1f14c-183">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1f14c-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-184">プロパティのタグ</span><span class="sxs-lookup"><span data-stu-id="1f14c-184">Tag Property</span></span>  <br/> |<span data-ttu-id="1f14c-185">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-185">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-186">予約済みのデータ</span><span class="sxs-lookup"><span data-stu-id="1f14c-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="1f14c-187">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-187">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-188">プロパティ値の和集合</span><span class="sxs-lookup"><span data-stu-id="1f14c-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="1f14c-189">値のデータ</span><span class="sxs-lookup"><span data-stu-id="1f14c-189">Value Data</span></span>  <br/> |<span data-ttu-id="1f14c-190">0 または変数 (プロパティ タグによって異なる)</span><span class="sxs-lookup"><span data-stu-id="1f14c-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="1f14c-191">プロパティ値の解釈</span><span class="sxs-lookup"><span data-stu-id="1f14c-191">Interpreting the Property Value</span></span>

<span data-ttu-id="1f14c-192">プロパティ値の和集合と値のデータは、プロパティ ブロックの最初の 4 バイトのプロパティのタグに基づいて解釈されます。</span><span class="sxs-lookup"><span data-stu-id="1f14c-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="1f14c-193">このプロパティのタグは、MAPI プロパティのタグと同じ形式になります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="1f14c-194">0 から 15 ビットのプロパティのタグがプロパティの種類です。</span><span class="sxs-lookup"><span data-stu-id="1f14c-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="1f14c-195">16 から 31 ビットまでがプロパティの識別子です。</span><span class="sxs-lookup"><span data-stu-id="1f14c-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="1f14c-196">プロパティの種類によって、残りのプロパティの読み取り方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="1f14c-197">静的な値</span><span class="sxs-lookup"><span data-stu-id="1f14c-197">Static Value</span></span>

<span data-ttu-id="1f14c-198">一部のプロパティには和集合のデータのみがあり、値のデータがありません。</span><span class="sxs-lookup"><span data-stu-id="1f14c-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="1f14c-199">以下が、(プロパティのタグに基づく) プロパティの種類それぞれにおける、8 バイトのプロパティの和集合データの解釈方法です:</span><span class="sxs-lookup"><span data-stu-id="1f14c-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="1f14c-200">**プロパティの種類**</span><span class="sxs-lookup"><span data-stu-id="1f14c-200">**Prop Type**</span></span>|<span data-ttu-id="1f14c-201">**プロパティの和集合の解釈**</span><span class="sxs-lookup"><span data-stu-id="1f14c-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="1f14c-202">PT_I2</span></span>  <br/> |<span data-ttu-id="1f14c-203">short int</span><span class="sxs-lookup"><span data-stu-id="1f14c-203">short int \*columns</span></span>  <br/> |
|<span data-ttu-id="1f14c-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1f14c-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="1f14c-205">long</span><span class="sxs-lookup"><span data-stu-id="1f14c-205">long</span></span>  <br/> |
|<span data-ttu-id="1f14c-206">PT_R4</span><span class="sxs-lookup"><span data-stu-id="1f14c-206">PT_R4</span></span>  <br/> |<span data-ttu-id="1f14c-207">浮動小数点数</span><span class="sxs-lookup"><span data-stu-id="1f14c-207">float</span></span>  <br/> |
|<span data-ttu-id="1f14c-208">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="1f14c-208">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="1f14c-209">double</span><span class="sxs-lookup"><span data-stu-id="1f14c-209">double</span></span>  <br/> |
|<span data-ttu-id="1f14c-210">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1f14c-210">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="1f14c-211">short int</span><span class="sxs-lookup"><span data-stu-id="1f14c-211">short int \*columns</span></span>  <br/> |
|<span data-ttu-id="1f14c-212">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="1f14c-212">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="1f14c-213">FILETIME</span><span class="sxs-lookup"><span data-stu-id="1f14c-213">FILETIME</span></span>  <br/> |
|<span data-ttu-id="1f14c-214">PT_I8</span><span class="sxs-lookup"><span data-stu-id="1f14c-214">PT_I8</span></span>  <br/> |<span data-ttu-id="1f14c-215">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="1f14c-215">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="1f14c-216">動的な値</span><span class="sxs-lookup"><span data-stu-id="1f14c-216">Dynamic Values</span></span>

<span data-ttu-id="1f14c-217">他のプロパティは、プロパティのタグ、予約済みのデータ、プロパティ値の和集合を含む最初の 16 バイトの次の値データのブロックにデータを持ちます。</span><span class="sxs-lookup"><span data-stu-id="1f14c-217">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="1f14c-218">静的な値とは異なり、8 バイトのプロパティ値の和集合に含まれているデータに関しては、読み取りは行われません。</span><span class="sxs-lookup"><span data-stu-id="1f14c-218">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="1f14c-219">書き込む場合は、これらの 8 バイトにデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="1f14c-219">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="1f14c-220">ただし、8 バイトのコンテンツは重要ではありません。</span><span class="sxs-lookup"><span data-stu-id="1f14c-220">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="1f14c-221">動的な値では、プロパティのタグの種類によって、値データの解釈方法が決まります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-221">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="1f14c-222">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="1f14c-222">PT_STRING8</span></span> 
  
|<span data-ttu-id="1f14c-223">**値データ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-223">**Value Data**</span></span>|<span data-ttu-id="1f14c-224">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1f14c-224">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-225">バイト n の数</span><span class="sxs-lookup"><span data-stu-id="1f14c-225">Number of bytes n</span></span>  <br/> |<span data-ttu-id="1f14c-226">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-226">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-227">ANSI 文字列 (NULL 終端文字を含む) として解釈されるバイト</span><span class="sxs-lookup"><span data-stu-id="1f14c-227">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="1f14c-228">n</span><span class="sxs-lookup"><span data-stu-id="1f14c-228">n</span></span>  <br/> |
   
<span data-ttu-id="1f14c-229">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="1f14c-229">PT_CLSID</span></span>
  
|<span data-ttu-id="1f14c-230">**値データ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-230">**Value Data**</span></span>|<span data-ttu-id="1f14c-231">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1f14c-231">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-232">GUID として解釈されるバイト</span><span class="sxs-lookup"><span data-stu-id="1f14c-232">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="1f14c-233">16</span><span class="sxs-lookup"><span data-stu-id="1f14c-233">-16</span></span>  <br/> |
|||
   
<span data-ttu-id="1f14c-234">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1f14c-234">PT_BINARY</span></span> 
  
|<span data-ttu-id="1f14c-235">**値データ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-235">**Value Data**</span></span>|<span data-ttu-id="1f14c-236">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1f14c-236">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-237">バイト n の数</span><span class="sxs-lookup"><span data-stu-id="1f14c-237">Number of bytes n</span></span>  <br/> |<span data-ttu-id="1f14c-238">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-238">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-239">バイト配列として解釈されるバイト</span><span class="sxs-lookup"><span data-stu-id="1f14c-239">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="1f14c-240">n</span><span class="sxs-lookup"><span data-stu-id="1f14c-240">n</span></span>  <br/> |
   
<span data-ttu-id="1f14c-241">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="1f14c-241">PT_ERROR</span></span>
  
|<span data-ttu-id="1f14c-242">**値データ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-242">**Value Data**</span></span>|<span data-ttu-id="1f14c-243">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1f14c-243">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-244">バイト n の数</span><span class="sxs-lookup"><span data-stu-id="1f14c-244">Number of bytes n</span></span>  <br/> |<span data-ttu-id="1f14c-245">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-245">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-246">バイト配列として解釈されるバイト</span><span class="sxs-lookup"><span data-stu-id="1f14c-246">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="1f14c-247">n</span><span class="sxs-lookup"><span data-stu-id="1f14c-247">n</span></span>  <br/> |
   
<span data-ttu-id="1f14c-248">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="1f14c-248">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="1f14c-249">**値データ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-249">**Value Data**</span></span>|<span data-ttu-id="1f14c-250">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1f14c-250">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-251">バイナリ配列 X の数</span><span class="sxs-lookup"><span data-stu-id="1f14c-251">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="1f14c-252">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-252">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-253">X バイナリ配列を含むバイトの実行。</span><span class="sxs-lookup"><span data-stu-id="1f14c-253">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="1f14c-254">各配列は、PT_BINARY バイトの実行とまったく同じ方法で解釈される必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-254">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="1f14c-255">変数</span><span class="sxs-lookup"><span data-stu-id="1f14c-255">Variable</span></span>  <br/> |
   
<span data-ttu-id="1f14c-256">PT_MV_STRING8 (Outlook 2007、Outlook 2010、Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="1f14c-256">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="1f14c-257">**値データ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-257">**Value Data**</span></span>|<span data-ttu-id="1f14c-258">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1f14c-258">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-259">ANSI 文字列 X の数</span><span class="sxs-lookup"><span data-stu-id="1f14c-259">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="1f14c-260">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-260">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-261">X ANSI 文字列を含むバイトの実行。</span><span class="sxs-lookup"><span data-stu-id="1f14c-261">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="1f14c-262">各文字列は、PT_STRING8 バイトの実行とまったく同じ方法で解釈される必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-262">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="1f14c-263">変数</span><span class="sxs-lookup"><span data-stu-id="1f14c-263">Variable</span></span>  <br/> |
   
<span data-ttu-id="1f14c-264">PT_MV_UNICODE (Outlook 2007、Outlook 2010、Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="1f14c-264">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="1f14c-265">**値データ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-265">**Value Data**</span></span>|<span data-ttu-id="1f14c-266">**バイト数**</span><span class="sxs-lookup"><span data-stu-id="1f14c-266">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f14c-267">Unicode 文字列 X の数</span><span class="sxs-lookup"><span data-stu-id="1f14c-267">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="1f14c-268">4</span><span class="sxs-lookup"><span data-stu-id="1f14c-268">-4</span></span>  <br/> |
|<span data-ttu-id="1f14c-269">X UNICODE 文字列を含むバイトの実行。</span><span class="sxs-lookup"><span data-stu-id="1f14c-269">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="1f14c-270">各文字列は、PT_UNICODE バイトの実行とまったく同じ方法で解釈される必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-270">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="1f14c-271">変数</span><span class="sxs-lookup"><span data-stu-id="1f14c-271">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="1f14c-272">重要なプロパティ</span><span class="sxs-lookup"><span data-stu-id="1f14c-272">Significant properties</span></span>

<span data-ttu-id="1f14c-273">このトピックで前述したように、プロパティを表すバイナリのブロックには、アドレス帳の受信者のプロパティに対応するプロパティ タグがあります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-273">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="1f14c-274">ここに記載されていないプロパティについては、http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx の説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1f14c-274">For properties that are not listed here, you can look up the property description at http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="1f14c-275">**プロパティ名**</span><span class="sxs-lookup"><span data-stu-id="1f14c-275">**Property Name**</span></span>|<span data-ttu-id="1f14c-276">**プロパティのタグ**</span><span class="sxs-lookup"><span data-stu-id="1f14c-276">**Tag Property**</span></span>|<span data-ttu-id="1f14c-277">**説明 (詳細については、MSDN を参照してください)**</span><span class="sxs-lookup"><span data-stu-id="1f14c-277">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1f14c-278">PR_NICK_NAME_W (オートコンプリート ストリーム専用で、受信者には送信されません)</span><span class="sxs-lookup"><span data-stu-id="1f14c-278">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="1f14c-279">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="1f14c-279">0x6001001f</span></span>  <br/> |<span data-ttu-id="1f14c-280">このプロパティは、それぞれの受信者の行の先頭である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-280">This property must be first in each recipient row.</span></span> <span data-ttu-id="1f14c-281">受信者の行のキー識別子として機能します。</span><span class="sxs-lookup"><span data-stu-id="1f14c-281">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="1f14c-282">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="1f14c-282">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="1f14c-283">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="1f14c-283">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="1f14c-284">受信者のアドレス帳エントリの識別子です。</span><span class="sxs-lookup"><span data-stu-id="1f14c-284">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="1f14c-285">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="1f14c-285">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="1f14c-286">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="1f14c-286">0x3001001F</span></span>  <br/> |<span data-ttu-id="1f14c-287">受信者の表示名です。</span><span class="sxs-lookup"><span data-stu-id="1f14c-287">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="1f14c-288">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="1f14c-288">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="1f14c-289">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="1f14c-289">0x3003001F</span></span>  <br/> |<span data-ttu-id="1f14c-290">受信者のメール アドレス (例: johndoe@contoso.com または /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span><span class="sxs-lookup"><span data-stu-id="1f14c-290">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="1f14c-291">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="1f14c-291">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="1f14c-292">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="1f14c-292">0x3002001F</span></span>  <br/> |<span data-ttu-id="1f14c-293">受信者のアドレスの種類です (例: SMTP または EX)。</span><span class="sxs-lookup"><span data-stu-id="1f14c-293">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="1f14c-294">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="1f14c-294">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="1f14c-295">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="1f14c-295">0x300B0102</span></span>  <br/> |<span data-ttu-id="1f14c-296">受信者の MAPI 検索キーです。</span><span class="sxs-lookup"><span data-stu-id="1f14c-296">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="1f14c-297">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="1f14c-297">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="1f14c-298">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="1f14c-298">0x39FE001f</span></span>  <br/> |<span data-ttu-id="1f14c-299">受信者の SMTP アドレスです。</span><span class="sxs-lookup"><span data-stu-id="1f14c-299">The recipient's email address.</span></span>  <br/> |
|<span data-ttu-id="1f14c-300">PR_DROPDOWN_DISPLAY_NAME_W (オートコンプリート ストリーム専用で、受信者には送信されません)</span><span class="sxs-lookup"><span data-stu-id="1f14c-300">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="1f14c-301">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="1f14c-301">0X6003001f</span></span>  <br/> |<span data-ttu-id="1f14c-302">表示文字列で、オートコンプリート一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1f14c-302">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="1f14c-303">PR_NICK_NAME_WEIGHT (オートコンプリート ストリーム専用で、受信者には送信されません)</span><span class="sxs-lookup"><span data-stu-id="1f14c-303">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="1f14c-304">0x60040003</span><span class="sxs-lookup"><span data-stu-id="1f14c-304">0x60040003</span></span>  <br/> |<span data-ttu-id="1f14c-305">このオートコンプリートの入力のウェイトです。</span><span class="sxs-lookup"><span data-stu-id="1f14c-305">The weight of this autocomplete entry.</span></span> <span data-ttu-id="1f14c-306">オートコンプリート一覧と一致する場合のオートコンプリート入力順序を決定するときに、このウェイトを使用します。</span><span class="sxs-lookup"><span data-stu-id="1f14c-306">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="1f14c-307">高いウェイトの入力が、低いウェイトの入力よりも先に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1f14c-307">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="1f14c-308">完全なオートコンプリート一覧はこのプロパティによって並べ替えが行われます。</span><span class="sxs-lookup"><span data-stu-id="1f14c-308">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="1f14c-309">時間が経つにつれウェイトは減少しますが、この受信者にユーザーがメールを送信するとウェイトが増加します。</span><span class="sxs-lookup"><span data-stu-id="1f14c-309">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="1f14c-310">このプロパティの詳細については、このトピックの後半に記載されている説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1f14c-310">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="1f14c-311">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="1f14c-311">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="1f14c-312">オートコンプリート ストリームの行の一式は、PR_NICK_NAME_WEIGHT によって降順に並べ替えられます。オートコンプリート ストリームは常にこの並べ替えられた内容を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-312">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="1f14c-313">したがって、行のウェイトを変更するときは必ず、行の位置が行全体で並べ替えられた順序と一致しているかどうかを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-313">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="1f14c-314">行セットへの追加を行うときは、並べ替えの順序を乱さないように正しい位置に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f14c-314">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="1f14c-315">このウェイトの最小値は 0x1 で、最大値は LONG_MAX です。</span><span class="sxs-lookup"><span data-stu-id="1f14c-315">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="1f14c-316">他のウェイトの値は無効と見なされます。</span><span class="sxs-lookup"><span data-stu-id="1f14c-316">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="1f14c-317">Outlook 2007 によってメールが送信されたり受信者が解決された場合、その受信者のウェイトは 0x2000 ずつ増加します。</span><span class="sxs-lookup"><span data-stu-id="1f14c-317">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

