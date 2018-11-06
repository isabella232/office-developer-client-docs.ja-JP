---
title: DBEngine.CompactDatabase メソッド (DAO)
TOCTitle: CompactDatabase Method
ms:assetid: 03f3a156-005a-4b71-81b0-598f326f7d42
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844821(v=office.15)
ms:contentKeyID: 48542997
ms.date: 10/24/2016
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052936
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fb3deeb6e2f90c6ddbe7cdc90c5e599349ebfb10
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998722"
---
# <a name="dbenginecompactdatabase-method-dao"></a><span data-ttu-id="7e33d-102">DBEngine.CompactDatabase メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="7e33d-102">DBEngine.CompactDatabase method (DAO)</span></span>

<span data-ttu-id="7e33d-103">**適用されます**Access 2013 |。アクセス 2016</span><span class="sxs-lookup"><span data-stu-id="7e33d-103">**Applies to**: Access 2013 | Access 2016</span></span>

<span data-ttu-id="7e33d-104">コピーし、閉じたデータベースを最適化およびそのバージョン、照合の順序、および暗号化を変更するオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-104">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="7e33d-105">します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="7e33d-105">(Microsoft Access workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="7e33d-106">操作、更新、および SQL クエリを [SQL 更新ステートメント (CurrentDb.Execute [更新])] などの暗号化されたリンク テーブルを使用している場合は、暗号化キーを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e33d-106">When using encrypted linked tables for action, update, and SQL queries [such as a SQL UPDATE statement (CurrentDb.Execute "UPDATE...")], you must supply the encryption key.</span></span> <span data-ttu-id="7e33d-107">また、リンク テーブルでは、暗号化キーの 19 文字制限があります。</span><span class="sxs-lookup"><span data-stu-id="7e33d-107">Also, linked tables have a 19-character limit for the encryption key.</span></span> <span data-ttu-id="7e33d-108">このトピックの最後に**暗号化されたリンク テーブル**のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e33d-108">See the **Encrypted linked tables** section at the end of this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e33d-109">構文</span><span class="sxs-lookup"><span data-stu-id="7e33d-109">Syntax</span></span>

<span data-ttu-id="7e33d-110">*式*です。CompactDatabase (***SrcName***、 ***DstName***、 ***DstLocale***、***オプション***、***パスワード***)</span><span class="sxs-lookup"><span data-stu-id="7e33d-110">*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)</span></span>

<span data-ttu-id="7e33d-111">\*式\***DBEngine**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-111">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e33d-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7e33d-112">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e33d-113">名前</span><span class="sxs-lookup"><span data-stu-id="7e33d-113">Name</span></span></p></th>
<th><p><span data-ttu-id="7e33d-114">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="7e33d-114">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7e33d-115">データ型</span><span class="sxs-lookup"><span data-stu-id="7e33d-115">Data type</span></span></p></th>
<th><p><span data-ttu-id="7e33d-116">説明</span><span class="sxs-lookup"><span data-stu-id="7e33d-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-117"><em>SrcName</em></span><span class="sxs-lookup"><span data-stu-id="7e33d-117"><em>SrcName</em></span></span></p></td>
<td><p><span data-ttu-id="7e33d-118">必須</span><span class="sxs-lookup"><span data-stu-id="7e33d-118">Required</span></span></p></td>
<td><p><span data-ttu-id="7e33d-119"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-120">既存の閉じているデータベースを識別します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-120">Identifies an existing, closed database.</span></span> <span data-ttu-id="7e33d-121">できます、完全なパスとファイル名の場合は、次のように&quot;C:\db1.mdb&quot;。</span><span class="sxs-lookup"><span data-stu-id="7e33d-121">It can be a full path and file name, such as &quot;C:\db1.mdb&quot;.</span></span> <span data-ttu-id="7e33d-122">ファイル名に拡張子が含まれる場合、それも指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e33d-122">If the file name has an extension, you must specify it.</span></span> <span data-ttu-id="7e33d-123">ネットワークでサポートされている場合は、指定することもネットワーク パスでは、次のように&quot; \\server1\share1\dir1\db1.mdb&quot;</span><span class="sxs-lookup"><span data-stu-id="7e33d-123">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1.mdb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-124"><em>DstName</em></span><span class="sxs-lookup"><span data-stu-id="7e33d-124"><em>DstName</em></span></span></p></td>
<td><p><span data-ttu-id="7e33d-125">必須</span><span class="sxs-lookup"><span data-stu-id="7e33d-125">Required</span></span></p></td>
<td><p><span data-ttu-id="7e33d-126"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-126"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-p104">作成中の最適化されたデータベースのファイル名およびそのパス。ネットワーク パスを指定することもできます。この引数を使用して、SrcName と同じデータベース ファイルを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="7e33d-p104">the file name (and path) of the compacted database that you're creating. You can also specify a network path. You can't use this argument to specify the same database file as SrcName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-130"><em>DstLocale</em></span><span class="sxs-lookup"><span data-stu-id="7e33d-130"><em>DstLocale</em></span></span></p></td>
<td><p><span data-ttu-id="7e33d-131">省略可能</span><span class="sxs-lookup"><span data-stu-id="7e33d-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="7e33d-132"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-132"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-133">「解説」に指定されているように、DstName の作成のための照合順序を指定する文字列式。</span><span class="sxs-lookup"><span data-stu-id="7e33d-133">A string expression that specifies a collating order for creating DstName, as specified in Remarks.</span></span></p>
<ul>
<li><p><span data-ttu-id="7e33d-134">この引数を省略すると、DstName のロケールは SrcName と同じになります。</span><span class="sxs-lookup"><span data-stu-id="7e33d-134">If you omit this argument, the locale of DstName is the same as SrcName.</span></span></p></li>
<li><p><span data-ttu-id="7e33d-135">パスワード文字列を連結することによって、DstName のパスワードを作成することもできます (で始まる&quot;; pwd =&quot;) を次のように、DstLocale の引数の定数: dbLangSpanish &amp; &quot;; pwd = NewPassword&quot;。</span><span class="sxs-lookup"><span data-stu-id="7e33d-135">You can also create a password for DstName by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the DstLocale argument, like this: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</span></span></p></li>
<li><p><span data-ttu-id="7e33d-136">SrcName (既定値) と同じ DstLocale を使用していますが、新しいパスワードを指定する場合は、DstLocale のパスワード文字列を入力するだけで: &quot;; pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="7e33d-136">If you want to use the same DstLocale as SrcName (the default value), but specify a new password, simply enter a password string for DstLocale: &quot;;pwd=NewPassword&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-137"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="7e33d-137"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="7e33d-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="7e33d-138">Optional</span></span></p></td>
<td><p><span data-ttu-id="7e33d-139"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-139"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-p105">省略可能。解説に指定されているように、1 つ以上のオプションを示す定数または定数の組み合わせ。対応する定数を加算すると、オプションを組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="7e33d-p105">Optional. A constant or combination of constants that indicates one or more options, as specified in Remarks. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-143"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="7e33d-143"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="7e33d-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="7e33d-144">Optional</span></span></p></td>
<td><p><span data-ttu-id="7e33d-145"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-145"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-146">データベースが暗号化されている場合に、暗号化キーを含む文字列式です。</span><span class="sxs-lookup"><span data-stu-id="7e33d-146">A string expression containing an encryption key, if the database is encrypted.</span></span> <span data-ttu-id="7e33d-147">文字列&quot;; pwd =&quot;実際のパスワードを付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e33d-147">The string &quot;;pwd=&quot; must precede the actual password.</span></span> <span data-ttu-id="7e33d-148">パスワード設定を DstLocale に含めると、この設定は無視されます。</span><span class="sxs-lookup"><span data-stu-id="7e33d-148">If you include a password setting in DstLocale, this setting is ignored.</span></span></p><p><span data-ttu-id="7e33d-149"><strong>注</strong>: これは非推奨のパラメーターでありでサポートされていません。ACCDB 形式です。</span><span class="sxs-lookup"><span data-stu-id="7e33d-149"><strong>NOTE</strong>: This is deprecated parameter and is not supported in .ACCDB format.</span></span> <span data-ttu-id="7e33d-150">暗号化します。ACCDB ファイルを使用して、"pwd ="オプション文字列。</span><span class="sxs-lookup"><span data-stu-id="7e33d-150">To encrypt an .ACCDB file, use the "pwd=" option string.</span></span> <span data-ttu-id="7e33d-151">[!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。</span><span class="sxs-lookup"><span data-stu-id="7e33d-151">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="7e33d-152">これらの文字を混在させたものになっていないパスワードは強固とはいえません。</span><span class="sxs-lookup"><span data-stu-id="7e33d-152">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="7e33d-153">たとえば、Y6dh!et5 は安全性の高いパスワードです。</span><span class="sxs-lookup"><span data-stu-id="7e33d-153">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="7e33d-154">House27 は推測されやすいパスワードです。</span><span class="sxs-lookup"><span data-stu-id="7e33d-154">Weak password: House27.</span></span> <span data-ttu-id="7e33d-155">また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="7e33d-155">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7e33d-156">解説</span><span class="sxs-lookup"><span data-stu-id="7e33d-156">Remarks</span></span>

<span data-ttu-id="7e33d-157">次の定数のいずれかを DstLocale 引数に使用して、テキストの文字列比較を行う **CollatingOrder** プロパティを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7e33d-157">You can use one of the following constants for the DstLocale argument to specify the **CollatingOrder** property for string comparisons of text.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e33d-158">定数</span><span class="sxs-lookup"><span data-stu-id="7e33d-158">Constant</span></span></p></th>
<th><p><span data-ttu-id="7e33d-159">照合順序</span><span class="sxs-lookup"><span data-stu-id="7e33d-159">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-160"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-160"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-161">英語、ドイツ語、フランス語、ポルトガル語、イタリア語、現代スペイン語</span><span class="sxs-lookup"><span data-stu-id="7e33d-161">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-162"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-162"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-163">アラビア語</span><span class="sxs-lookup"><span data-stu-id="7e33d-163">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-164"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-164"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-165">簡体字中国語</span><span class="sxs-lookup"><span data-stu-id="7e33d-165">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-166"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-166"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-167">繁体字中国語</span><span class="sxs-lookup"><span data-stu-id="7e33d-167">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-168"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-168"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-169">ロシア語</span><span class="sxs-lookup"><span data-stu-id="7e33d-169">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-170"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-170"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-171">チェコ語</span><span class="sxs-lookup"><span data-stu-id="7e33d-171">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-172"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-172"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-173">オランダ語</span><span class="sxs-lookup"><span data-stu-id="7e33d-173">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-174"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-174"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-175">ギリシャ語</span><span class="sxs-lookup"><span data-stu-id="7e33d-175">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-176"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-176"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-177">ヘブライ語</span><span class="sxs-lookup"><span data-stu-id="7e33d-177">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-178"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-178"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-179">ハンガリー語</span><span class="sxs-lookup"><span data-stu-id="7e33d-179">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-180"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-180"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-181">アイスランド語</span><span class="sxs-lookup"><span data-stu-id="7e33d-181">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-182"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-182"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-183">日本語</span><span class="sxs-lookup"><span data-stu-id="7e33d-183">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-184"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-184"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-185">韓国語</span><span class="sxs-lookup"><span data-stu-id="7e33d-185">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-186"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-186"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-187">北欧諸国語 (Microsoft Jet データベース エンジン バージョン 1.0 のみ)</span><span class="sxs-lookup"><span data-stu-id="7e33d-187">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-188"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-188"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-189">ノルウェー語およびデンマーク語</span><span class="sxs-lookup"><span data-stu-id="7e33d-189">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-190"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-190"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-191">ポーランド語</span><span class="sxs-lookup"><span data-stu-id="7e33d-191">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-192"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-192"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-193">スロベニア語</span><span class="sxs-lookup"><span data-stu-id="7e33d-193">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-194"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-194"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-195">古スペイン語</span><span class="sxs-lookup"><span data-stu-id="7e33d-195">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-196"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-196"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-197">スウェーデン語およびフィンランド語</span><span class="sxs-lookup"><span data-stu-id="7e33d-197">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-198"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-198"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-199">タイ語</span><span class="sxs-lookup"><span data-stu-id="7e33d-199">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-200"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-200"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-201">トルコ語</span><span class="sxs-lookup"><span data-stu-id="7e33d-201">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="7e33d-202">引数 options に以下のいずれかの定数を使用すると、最適化する際に暗号化するか、または解読するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7e33d-202">You can use one of the following constants in the options argument to specify whether to encrypt or to decrypt the database while it's compacted.</span></span>

> [!NOTE]
> <span data-ttu-id="7e33d-203">定数 dbEncrypt と dbDecrypt は非推奨しでサポートされていません。ACCDB ファイル形式です。</span><span class="sxs-lookup"><span data-stu-id="7e33d-203">The constants dbEncrypt and dbDecrypt are deprecated and not supported in .ACCDB file formats.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e33d-204">定数</span><span class="sxs-lookup"><span data-stu-id="7e33d-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="7e33d-205">説明</span><span class="sxs-lookup"><span data-stu-id="7e33d-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-206"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-206"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-207">最適化中にデータベースを暗号化します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-207">Encrypt the database while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-208"><strong>dbDecrypt</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-208"><strong>dbDecrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-209">最適化中にデータベースを解読します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-209">Decrypt the database while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="7e33d-210">暗号化の定数を省略するか、または **dbDecrypt** と **dbEncrypt** の両方を指定すると、DstName の暗号化の設定は SrcName と同じになります。</span><span class="sxs-lookup"><span data-stu-id="7e33d-210">If you omit an encryption constant or if you include both **dbDecrypt** and **dbEncrypt**, DstName will have the same encryption as SrcName.</span></span>

<span data-ttu-id="7e33d-p108">引数 options に次のいずれかの定数を使用すると、最適化されたデータベースのデータの形式のバージョンを指定できます。この定数は、DstName のデータ形式のバージョンだけに影響し、フォーム、レポートなどの Microsoft Access によって定義されたオブジェクトのバージョンには影響しません。</span><span class="sxs-lookup"><span data-stu-id="7e33d-p108">You can use one of the following constants in the options argument to specify the version of the data format for the compacted database. This constant affects only the version of the data format of DstName and doesn't affect the version of any Microsoft Access-defined objects, such as forms and reports.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e33d-213">定数</span><span class="sxs-lookup"><span data-stu-id="7e33d-213">Constant</span></span></p></th>
<th><p><span data-ttu-id="7e33d-214">説明</span><span class="sxs-lookup"><span data-stu-id="7e33d-214">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-215"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-215"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-216">最適化に Microsoft Jet データベース エンジン バージョン 1.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-216">Creates a database that uses the Microsoft Jet database engine version 1.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-217"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-217"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-218">最適化に Microsoft Jet データベース エンジン バージョン 1.1 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-218">Creates a database that uses the Microsoft Jet database engine version 1.1 file format while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-219"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-219"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-220">最適化に Microsoft Jet データベース エンジン バージョン 2.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-220">Creates a database that uses the Microsoft Jet database engine version 2.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-221"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-221"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-222">最適化に Microsoft Jet データベース エンジン バージョン 3.0 のファイル形式 (バージョン 3.5 互換) を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-222">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5) while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e33d-223"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-223"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-224">最適化に Microsoft Jet データベース エンジン バージョン 4.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-224">Creates a database that uses the Microsoft Jet database engine version 4.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e33d-225"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="7e33d-225"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="7e33d-226">最適化に Microsoft Access データベース エンジン バージョン 12.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-226">Creates a database that uses the Microsoft Access database engine version 12.0 file format while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="7e33d-p109">指定できるバージョン定数は 1 つだけです。バージョン定数を省略すると、DstName には SrcName と同じバージョンが指定されます。DstName は、SrcName と同じかまたはそれ以降のバージョンのみに最適化できます。</span><span class="sxs-lookup"><span data-stu-id="7e33d-p109">You can specify only one version constant. If you omit a version constant, DstName will have the same version as SrcName. You can compact DstName only to a version that is the same or later than that of SrcName.</span></span>

<span data-ttu-id="7e33d-p110">データベースのデータを変更するに従って、データベースのファイルは断片化され、必要以上のディスク容量を使用する可能性があります。 **CompactDatabase** メソッドを定期的に実行すると、データベースを最適化してファイルの断片化を解消できます。一般的に、最適化されたデータベースは小さく、実行速度も向上します。データベースをコピーして最適化する間に、照合順序、暗号化、およびデータ形式のバージョンを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="7e33d-p110">As you change data in a database, the database file can become fragmented and use more disk space than is necessary. Periodically, you can use the **CompactDatabase** method to compact your database to defragment the database file. The compacted database is usually smaller and often runs faster. You can also change the collating order, the encryption, or the version of the data format while you copy and compact the database.</span></span>

<span data-ttu-id="7e33d-p111">データベースを最適化する前に SrcName を閉じる必要があります。マルチユーザー環境では、最適化中に他のユーザーは SrcName を開くことはできません。SrcName が閉じていないか、または排他的に使用できない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7e33d-p111">You must close SrcName before you compact it. In a multiuser environment, other users can't have SrcName open while you're compacting it. If SrcName isn't closed or isn't available for exclusive use, an error occurs.</span></span>

<span data-ttu-id="7e33d-p112">**CompactDatabase** メソッドはデータベースのコピーを作成するので、元のデータベースとデータベースのコピーに対して十分なディスク容量が必要です。十分なディスク空き容量がない場合、最適化の操作は失敗します。複製する DstName のデータベースは、SrcName と同じディスクに保存する必要はありません。データベースの最適化が正常に終了した後に、元の SrcName ファイルを削除し、最適化された DstName ファイルを元のファイル名に変更できます。</span><span class="sxs-lookup"><span data-stu-id="7e33d-p112">Because **CompactDatabase** creates a copy of the database, you must have enough disk space for both the original and the duplicate databases. The compact operation fails if there isn't enough disk space available. The DstName duplicate database doesn't have to be on the same disk as SrcName. After successfully compacting a database, you can delete the SrcName file and rename the compacted DstName file to the original file name.</span></span>

<span data-ttu-id="7e33d-241">**CompactDatabase** メソッドは、SrcName に指定されているデータベースから DstName に指定されているデータベースにすべてのデータおよびセキュリティ アクセス許可の設定をコピーします。</span><span class="sxs-lookup"><span data-stu-id="7e33d-241">The **CompactDatabase** method copies all the data and the security permission settings from the database specified by SrcName to the database specified by DstName.</span></span>

> [!NOTE]
> <span data-ttu-id="7e33d-242">[!メモ] **CompactDatabase** メソッドは Microsoft Access オブジェクトを変換できないので、 **CompactDatabase** メソッドを使用してこのようなオブジェクトを含むデータベースを変換しないでください。</span><span class="sxs-lookup"><span data-stu-id="7e33d-242">Because the **CompactDatabase** method doesn't convert Microsoft Access objects, you shouldn't use **CompactDatabase** to convert a database containing such objects.</span></span>

## <a name="encrypted-linked-tables"></a><span data-ttu-id="7e33d-243">暗号化されたリンク テーブル</span><span class="sxs-lookup"><span data-stu-id="7e33d-243">Encrypted linked tables</span></span>

<span data-ttu-id="7e33d-p113">暗号化されたパスワードは、使用するデータベースのファイル形式に依存します。Access 2003 (.mdb) 以前のデータベースを使用している場合、データベースを保護するために 1 つのパスワードがあり、データベースを暗号化するために別のパスワードがあります。Access 2007 (.accdb) 以降 (.mdb) のデータベースでは、データベースを暗号化して保護するには 1 つのパスワードのみを使用します。2 つのパスワードを使用するオプションはなくなりました。</span><span class="sxs-lookup"><span data-stu-id="7e33d-p113">Encrypted passwords are dependent on the file format of the database that you are using. If you are using an Access 2003 (.mdb) or earlier database, you will have one password to protect the database, and a separate password to encrypt the database. For Access 2007 (.accdb) and later (.mdb) databases, the only option is to encrypt and protect the database with one password, as the option to have two separate passwords has been removed.</span></span>

> [!NOTE]
> <span data-ttu-id="7e33d-247">Access 2007 (.accdb) データベースの場合、パスワードは暗号化キーです。</span><span class="sxs-lookup"><span data-stu-id="7e33d-247">For Access 2007 (.accdb) databases, the password is the encryption key</span></span>

<span data-ttu-id="7e33d-248">コマンド ボタンには、次のサンプル VBA コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e33d-248">You can use the following example VBA code for a command button:</span></span>

```vb
    Private Sub Command0_Click()
    
    Dim strSourcePath As String
    Dim strDestPath As String
    
    strSourcePath = "<path>\sourceDb.accdb"
    strDestPath = "<path>\destDb.accdb"
    
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
    
    Set CurrentDatabase = CurrentDb
    Set LinkedTableDef = CurrentDatabase.CreateTableDef 
    ("My Linked Table")
    LinkedTableDef.Connect = "MS Access;pwd=Access";database=" & strDestPath
    LinkedTableDef.RefreshLink
    
    
    MsgBox "Finished"
    
    End Sub 
```

<br/>

<span data-ttu-id="7e33d-249">次のコード例は、CompactDatabase を使用して、パスワード (暗号化キー) を使用し、最適化されたデータベース内のテーブルにリンクする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7e33d-249">The following code sample shows how to use CompactDatabase with a password (encryption key) and then link to a table in that compacted database.</span></span> <span data-ttu-id="7e33d-250">パスワードを入力する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="7e33d-250">Note that a password must be supplied.</span></span>

```vb
    Private Sub CompactAndLink_Click() 
     
    Dim strSourcePath As String
    Dim strDestPath As String
    Dim strSourceTableName As String
    Dim strDestTableName As String
    Dim tdf As TableDef
     
    strSourcePath = "<path>\<database>.accdb"
    strDestPath = "<path>\<database>.accdb"
    strSourceTableName = "<table name in destination database>"
    strDestTableName = "<linked table name>"
     
    ' Compact source database into new destination database with encrypted password
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
     
    ' Link to one of the tables in the destination database
    ' Password must be provided in the Connect property
     
    Set CurrentDatabase = CurrentDb
    Set tdf = CurrentDatabase.CreateTableDef(strDestTableName)
       
        With tdf
            .Connect = ";pwd=Access" & ";DATABASE=" & strDestPath
            .SourceTableName = strSourceTableName
        End With
        
    CurrentDatabase.TableDefs.Append tdf
     
    MsgBox "Database compacted and encrypted password applied. Link to table also completed."
     
    End Sub
```
