---
title: DBEngine.CompactDatabaseメソッド（DAO）
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
localization_priority: Priority
ms.openlocfilehash: b50cb0453df1fa357fbd0b089af2e74fdd4b4c1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294338"
---
# <a name="dbenginecompactdatabase-method-dao"></a><span data-ttu-id="3db13-102">DBEngine.CompactDatabaseメソッド（DAO）</span><span class="sxs-lookup"><span data-stu-id="3db13-102">DBEngine.CompactDatabase Method (DAO)</span></span>

<span data-ttu-id="3db13-103">**適応対象**: Access 2013 | Access 2016</span><span class="sxs-lookup"><span data-stu-id="3db13-103">**Applies to:** Access 2013 | Access 2016</span></span>

<span data-ttu-id="3db13-104">閉じたデータベースをコピーして圧縮し、そのバージョン、照合順、および暗号化方式を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="3db13-104">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption. (Microsoft Access workspaces only). 
.</span></span> <span data-ttu-id="3db13-105">（Microsoft Access作業領域のみ）</span><span class="sxs-lookup"><span data-stu-id="3db13-105">Table (Microsoft Access workspaces only)</span></span>

> [!NOTE]
> <span data-ttu-id="3db13-106">リンクされている暗号化されたテーブルを、アクション、更新、SQL クエリ [SQL UPDATE文 (CurrentDb.Execute "UPDATE...") など] に使用する場合、暗号化キーを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3db13-106">When using encrypted linked tables for action, update, and SQL queries [such as a SQL UPDATE statement (CurrentDb.Execute "UPDATE...")], you must supply the encryption key.</span></span> <span data-ttu-id="3db13-107">リンクされているテーブルに対する暗号化キーは 19 文字に制限されています。</span><span class="sxs-lookup"><span data-stu-id="3db13-107">Also, linked tables have a 19-character limit for the encryption key.</span></span> <span data-ttu-id="3db13-108">このトピックの終わりにある「**暗号化されたリンク テーブル**」のセクションをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3db13-108">See the **Encrypted linked tables** section at the end of this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="3db13-109">構文</span><span class="sxs-lookup"><span data-stu-id="3db13-109">Syntax</span></span>

<span data-ttu-id="3db13-110">*式* .CompactDatabase（\*\*\* SrcName ***、*** DstName ***、***DstLocale***、***オプション***、***パスワード\*\*\*）</span><span class="sxs-lookup"><span data-stu-id="3db13-110">CompactDatabase(\*\*\*\*SrcName\*\*\*\*, ***DstName***, ***DstLocale, \*\*\*\*\*\*Options, \*\*\*\*\*\*password***)</span></span>

<span data-ttu-id="3db13-111">*式* **DBEngine**オブジェクトを返す式。</span><span class="sxs-lookup"><span data-stu-id="3db13-111">*expression*  An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3db13-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3db13-112">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3db13-113">名前</span><span class="sxs-lookup"><span data-stu-id="3db13-113">Name</span></span></p></th>
<th><p><span data-ttu-id="3db13-114">必須かどうか</span><span class="sxs-lookup"><span data-stu-id="3db13-114">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="3db13-115">データ型</span><span class="sxs-lookup"><span data-stu-id="3db13-115">Data type</span></span></p></th>
<th><p><span data-ttu-id="3db13-116">説明</span><span class="sxs-lookup"><span data-stu-id="3db13-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3db13-117"><em>SrcName</em></span><span class="sxs-lookup"><span data-stu-id="3db13-117"><em>SrcName</em></span></span></p></td>
<td><p><span data-ttu-id="3db13-118">必須</span><span class="sxs-lookup"><span data-stu-id="3db13-118">Required</span></span></p></td>
<td><p><span data-ttu-id="3db13-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-120">既存の閉じているデータベースを識別します。</span><span class="sxs-lookup"><span data-stu-id="3db13-120">Identifies an existing, closed database.</span></span> <span data-ttu-id="3db13-121">フルパスとファイル名（&quot;C:\db1.mdb&quot;など）でもかまいません。</span><span class="sxs-lookup"><span data-stu-id="3db13-121">It can be a full path and file name, such as "C:\db1.mdb".</span></span> <span data-ttu-id="3db13-122">ファイル名に拡張子が付いている場合は、それを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3db13-122">If the file name has an extension, you must specify it.</span></span> <span data-ttu-id="3db13-123">ネットワークでサポートされている場合は、&quot; \\server1\share1\dir1\ db1.mdb&quot;のようにネットワークパスも指定できます。</span><span class="sxs-lookup"><span data-stu-id="3db13-123">If your network supports it, you can also specify a network path, such as "server1\share1\dir1\db1.mdb"</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-124"><em>DstName</em></span><span class="sxs-lookup"><span data-stu-id="3db13-124"><em>DstName</em></span></span></p></td>
<td><p><span data-ttu-id="3db13-125">必須</span><span class="sxs-lookup"><span data-stu-id="3db13-125">Required</span></span></p></td>
<td><p><span data-ttu-id="3db13-126"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-126"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-p104">作成中の最適化されたデータベースのファイル名およびそのパス。ネットワーク パスを指定することもできます。この引数を使用して、SrcName と同じデータベース ファイルを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="3db13-p104">the file name (and path) of the compacted database that you're creating. You can also specify a network path. You can't use this argument to specify the same database file as SrcName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-130"><em>DstLocale</em></span><span class="sxs-lookup"><span data-stu-id="3db13-130"><em>DstLocale</em></span></span></p></td>
<td><p><span data-ttu-id="3db13-131">省略可能</span><span class="sxs-lookup"><span data-stu-id="3db13-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="3db13-132"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-132"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-133">「解説」に指定されているように、DstName の作成のための照合順序を指定する文字列式。</span><span class="sxs-lookup"><span data-stu-id="3db13-133">A string expression that specifies a collating order for creating DstName, as specified in Remarks.</span></span></p>
<ul>
<li><p><span data-ttu-id="3db13-134">この引数を省略すると、DstName のロケールは SrcName と同じになります。</span><span class="sxs-lookup"><span data-stu-id="3db13-134">If you omit this argument, the locale of DstName is the same as SrcName.</span></span></p></li>
<li><p><span data-ttu-id="3db13-135">次のように、パスワード文字列（&quot;;pwd=&quot;で始まる）をDstLocale引数の定数と連結して、DstNameのパスワードを作成することもできます。 たとえばこのような形です：dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</span><span class="sxs-lookup"><span data-stu-id="3db13-135">You can also create a password for DstName by concatenating the password string (starting with ";pwd=") with a constant in the DstLocale argument, like this: dbLangSpanish & ";pwd=NewPassword".</span></span></p></li>
<li><p><span data-ttu-id="3db13-136">SrcNameと同じDstLocale（デフォルト値）を使用したいものの、新しいパスワードを指定したい場合は、DstLocaleのパスワード文字列を入力するだけです：&quot;;pwd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="3db13-136">If you want to use the same DstLocale as SrcName (the default value), but specify a new password, simply enter a password string for DstLocale: &quot;";pwd=NewPassword"&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-137"><em>オプション</em></span><span class="sxs-lookup"><span data-stu-id="3db13-137"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="3db13-138">省略可能</span><span class="sxs-lookup"><span data-stu-id="3db13-138">Optional</span></span></p></td>
<td><p><span data-ttu-id="3db13-139"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-139"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-p105">省略可能。解説に指定されているように、1 つ以上のオプションを示す定数または定数の組み合わせ。対応する定数を加算すると、オプションを組み合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="3db13-p105">Optional. A constant or combination of constants that indicates one or more options, as specified in Remarks. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-143"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="3db13-143"><em>password</em></span></span></p></td>
<td><p><span data-ttu-id="3db13-144">省略可能</span><span class="sxs-lookup"><span data-stu-id="3db13-144">Optional</span></span></p></td>
<td><p><span data-ttu-id="3db13-145"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-145"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-146">暗号化キーを含む文字列式（データベースが暗号化されている場合）</span><span class="sxs-lookup"><span data-stu-id="3db13-146">A string expression containing an encryption key, if the database is encrypted.</span></span> <span data-ttu-id="3db13-147">文字列&quot;;pwd=&quot;は実際のパスワードの前に置かなければなりません。</span><span class="sxs-lookup"><span data-stu-id="3db13-147">The string ";pwd=" must precede the actual password.</span></span> <span data-ttu-id="3db13-148">DstLocaleにパスワード設定を含めると、この設定は無視されます。</span><span class="sxs-lookup"><span data-stu-id="3db13-148">If you include a password setting in DstLocale, this setting is ignored.</span></span></p><p><span data-ttu-id="3db13-149"><strong>注</strong>：これは推奨されないパラメーターであり、.ACCDB形式ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3db13-149"><strong>NOTE</strong>: This is deprecated parameter and is not supported in .ACCDB format.</span></span> <span data-ttu-id="3db13-150">.ACCDBファイルを暗号化するには、 "pwd ="オプション文字列を使用します。</span><span class="sxs-lookup"><span data-stu-id="3db13-150">To encrypt an .ACCDB file, use the "pwd=" option string.</span></span> <span data-ttu-id="3db13-151">[!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。</span><span class="sxs-lookup"><span data-stu-id="3db13-151">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="3db13-152">これらの文字を混在させたものになっていないパスワードは強固とはいえません。</span><span class="sxs-lookup"><span data-stu-id="3db13-152">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="3db13-153">たとえば、Y6dh!et5 は安全性の高いパスワードです。</span><span class="sxs-lookup"><span data-stu-id="3db13-153">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="3db13-154">House27 は推測されやすいパスワードです。</span><span class="sxs-lookup"><span data-stu-id="3db13-154">Weak password: House27.</span></span> <span data-ttu-id="3db13-155">強力なパスワードでありながら、書き留めておかなくても覚えておくことができるパスワードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="3db13-155">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3db13-156">注釈</span><span class="sxs-lookup"><span data-stu-id="3db13-156">Remarks</span></span>

<span data-ttu-id="3db13-157">次の定数のいずれかを DstLocale 引数に使用して、テキストの文字列比較を行う **CollatingOrder** プロパティを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3db13-157">You can use one of the following constants for the DstLocale argument to specify the **CollatingOrder** property for string comparisons of text.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3db13-158">定数</span><span class="sxs-lookup"><span data-stu-id="3db13-158">Constant</span></span></p></th>
<th><p><span data-ttu-id="3db13-159">照合順序</span><span class="sxs-lookup"><span data-stu-id="3db13-159">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3db13-160"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-160"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-161">英語、ドイツ語、フランス語、ポルトガル語、イタリア語、現代スペイン語</span><span class="sxs-lookup"><span data-stu-id="3db13-161">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-162"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-162"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-163">Arabic</span><span class="sxs-lookup"><span data-stu-id="3db13-163">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-164"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-164"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-165">簡体字中国語</span><span class="sxs-lookup"><span data-stu-id="3db13-165">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-166"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-166"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-167">繁体字中国語</span><span class="sxs-lookup"><span data-stu-id="3db13-167">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-168"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-168"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-169">ロシア語</span><span class="sxs-lookup"><span data-stu-id="3db13-169">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-170"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-170"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-171">チェコ語</span><span class="sxs-lookup"><span data-stu-id="3db13-171">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-172"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-172"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-173">オランダ語</span><span class="sxs-lookup"><span data-stu-id="3db13-173">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-174"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-174"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-175">ギリシャ語</span><span class="sxs-lookup"><span data-stu-id="3db13-175">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-176"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-176"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-177">ヘブライ語</span><span class="sxs-lookup"><span data-stu-id="3db13-177">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-178"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-178"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-179">ハンガリー語</span><span class="sxs-lookup"><span data-stu-id="3db13-179">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-180"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-180"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-181">アイスランド語</span><span class="sxs-lookup"><span data-stu-id="3db13-181">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-182"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-182"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-183">日本語</span><span class="sxs-lookup"><span data-stu-id="3db13-183">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-184"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-184"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-185">韓国語</span><span class="sxs-lookup"><span data-stu-id="3db13-185">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-186"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-186"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-187">北欧諸国語 (Microsoft Jet データベース エンジン バージョン 1.0 のみ)</span><span class="sxs-lookup"><span data-stu-id="3db13-187">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-188"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-188"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-189">ノルウェー語およびデンマーク語</span><span class="sxs-lookup"><span data-stu-id="3db13-189">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-190"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-190"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-191">ポーランド語</span><span class="sxs-lookup"><span data-stu-id="3db13-191">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-192"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-192"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-193">スロベニア語</span><span class="sxs-lookup"><span data-stu-id="3db13-193">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-194"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-194"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-195">古スペイン語</span><span class="sxs-lookup"><span data-stu-id="3db13-195">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-196"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-196"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-197">スウェーデン語およびフィンランド語</span><span class="sxs-lookup"><span data-stu-id="3db13-197">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-198"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-198"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-199">タイ語</span><span class="sxs-lookup"><span data-stu-id="3db13-199">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-200"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-200"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-201">トルコ語</span><span class="sxs-lookup"><span data-stu-id="3db13-201">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="3db13-202">引数 options に以下のいずれかの定数を使用すると、最適化する際に暗号化するか、または解読するかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="3db13-202">You can use one of the following constants in the options argument to specify whether to encrypt or to decrypt the database while it's compacted.</span></span>

> [!NOTE]
> <span data-ttu-id="3db13-203">定数dbEncryptおよびdbDecryptは非推奨であり、.ACCDBファイル形式ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3db13-203">The constants dbEncrypt and dbDecrypt are deprecated and not supported in .accdb file formats.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3db13-204">定数</span><span class="sxs-lookup"><span data-stu-id="3db13-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="3db13-205">説明</span><span class="sxs-lookup"><span data-stu-id="3db13-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3db13-206"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-206"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-207">最適化中にデータベースを暗号化します。</span><span class="sxs-lookup"><span data-stu-id="3db13-207">Encrypt the database while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-208"><strong>dbDecrypt</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-208"><strong>dbDecrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-209">最適化中にデータベースを解読します。</span><span class="sxs-lookup"><span data-stu-id="3db13-209">Decrypt the database while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="3db13-210">暗号化の定数を省略するか、または **dbDecrypt** と **dbEncrypt** の両方を指定すると、DstName の暗号化の設定は SrcName と同じになります。</span><span class="sxs-lookup"><span data-stu-id="3db13-210">If you omit an encryption constant or if you include both **dbDecrypt** and **dbEncrypt**, DstName will have the same encryption as SrcName.</span></span>

<span data-ttu-id="3db13-p108">引数 options に次のいずれかの定数を使用すると、最適化されたデータベースのデータの形式のバージョンを指定できます。この定数は、DstName のデータ形式のバージョンだけに影響し、フォーム、レポートなどの Microsoft Access によって定義されたオブジェクトのバージョンには影響しません。</span><span class="sxs-lookup"><span data-stu-id="3db13-p108">You can use one of the following constants in the options argument to specify the version of the data format for the compacted database. This constant affects only the version of the data format of DstName and doesn't affect the version of any Microsoft Access-defined objects, such as forms and reports.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3db13-213">定数</span><span class="sxs-lookup"><span data-stu-id="3db13-213">Constant</span></span></p></th>
<th><p><span data-ttu-id="3db13-214">説明</span><span class="sxs-lookup"><span data-stu-id="3db13-214">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3db13-215"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-215"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-216">最適化に Microsoft Jet データベース エンジン バージョン 1.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="3db13-216">Creates a database that uses the Microsoft Jet database engine version 1.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-217"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-217"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-218">最適化に Microsoft Jet データベース エンジン バージョン 1.1 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="3db13-218">Creates a database that uses the Microsoft Jet database engine version 1.1 file format while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-219"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-219"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-220">最適化に Microsoft Jet データベース エンジン バージョン 2.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="3db13-220">Creates a database that uses the Microsoft Jet database engine version 2.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-221"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-221"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-222">最適化に Microsoft Jet データベース エンジン バージョン 3.0 のファイル形式 (バージョン 3.5 互換) を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="3db13-222">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5) while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3db13-223"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-223"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-224">最適化に Microsoft Jet データベース エンジン バージョン 4.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="3db13-224">Creates a database that uses the Microsoft Jet database engine version 4.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3db13-225"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="3db13-225"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="3db13-226">最適化に Microsoft Access データベース エンジン バージョン 12.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="3db13-226">Creates a database that uses the Microsoft Access database engine version 12.0 file format while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="3db13-p109">指定できるバージョン定数は 1 つだけです。バージョン定数を省略すると、DstName には SrcName と同じバージョンが指定されます。DstName は、SrcName と同じかまたはそれ以降のバージョンのみに最適化できます。</span><span class="sxs-lookup"><span data-stu-id="3db13-p109">You can specify only one version constant. If you omit a version constant, DstName will have the same version as SrcName. You can compact DstName only to a version that is the same or later than that of SrcName.</span></span>

<span data-ttu-id="3db13-p110">データベースのデータを変更するに従って、データベースのファイルは断片化され、必要以上のディスク容量を使用する可能性があります。**CompactDatabase** メソッドを定期的に実行すると、データベースを最適化してファイルの断片化を解消できます。一般的に、最適化されたデータベースは小さく、実行速度も向上します。データベースをコピーして最適化する間に、照合順序、暗号化、およびデータ形式のバージョンを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="3db13-p110">As you change data in a database, the database file can become fragmented and use more disk space than is necessary. Periodically, you can use the **CompactDatabase** method to compact your database to defragment the database file. The compacted database is usually smaller and often runs faster. You can also change the collating order, the encryption, or the version of the data format while you copy and compact the database.</span></span>

<span data-ttu-id="3db13-p111">データベースを最適化する前に SrcName を閉じる必要があります。マルチユーザー環境では、最適化中に他のユーザーは SrcName を開くことはできません。SrcName が閉じていないか、または排他的に使用できない場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="3db13-p111">You must close SrcName before you compact it. In a multiuser environment, other users can't have SrcName open while you're compacting it. If SrcName isn't closed or isn't available for exclusive use, an error occurs.</span></span>

<span data-ttu-id="3db13-p112">             \*\*CompactDatabase\*\* メソッドはデータベースのコピーを作成するので、元のデータベースとデータベースのコピーに対して十分なディスク容量が必要です。十分なディスク空き容量がない場合、最適化の操作は失敗します。複製する DstName のデータベースは、SrcName と同じディスクに保存する必要はありません。データベースの最適化が正常に終了した後に、元の SrcName ファイルを削除し、最適化された DstName ファイルを元のファイル名に変更できます。</span><span class="sxs-lookup"><span data-stu-id="3db13-p112">Because **CompactDatabase** creates a copy of the database, you must have enough disk space for both the original and the duplicate databases. The compact operation fails if there isn't enough disk space available. The DstName duplicate database doesn't have to be on the same disk as SrcName. After successfully compacting a database, you can delete the SrcName file and rename the compacted DstName file to the original file name.</span></span>

<span data-ttu-id="3db13-241">             \*\*CompactDatabase\*\* メソッドは、SrcName に指定されているデータベースから DstName に指定されているデータベースにすべてのデータおよびセキュリティ アクセス許可の設定をコピーします。</span><span class="sxs-lookup"><span data-stu-id="3db13-241">The **CompactDatabase** method copies all the data and the security permission settings from the database specified by SrcName to the database specified by DstName.</span></span>

> [!NOTE]
> <span data-ttu-id="3db13-242">**CompactDatabase** メソッドは Microsoft Access オブジェクトを変換できないので、**CompactDatabase** メソッドを使用してこのようなオブジェクトを含むデータベースを変換しないでください。</span><span class="sxs-lookup"><span data-stu-id="3db13-242">Because the **CompactDatabase** method doesn't convert Microsoft Access objects, you shouldn't use **CompactDatabase** to convert a database containing such objects.</span></span>

## <a name="encrypted-linked-tables"></a><span data-ttu-id="3db13-243">暗号化されたリンク テーブル</span><span class="sxs-lookup"><span data-stu-id="3db13-243">Encrypted linked tables</span></span>

<span data-ttu-id="3db13-p113">暗号化されたパスワードは、使用するデータベースのファイル形式に依存します。Access 2003 (.mdb) 以前のデータベースを使用している場合、データベースを保護するために 1 つのパスワードがあり、データベースを暗号化するために別のパスワードがあります。Access 2007 (.accdb) 以降 (.mdb) のデータベースでは、データベースを暗号化して保護するには 1 つのパスワードのみを使用します。2 つのパスワードを使用するオプションはなくなりました。</span><span class="sxs-lookup"><span data-stu-id="3db13-p113">Encrypted passwords are dependent on the file format of the database that you are using. If you are using an Access 2003 (.mdb) or earlier database, you will have one password to protect the database, and a separate password to encrypt the database. For Access 2007 (.accdb) and later (.mdb) databases, the only option is to encrypt and protect the database with one password, as the option to have two separate passwords has been removed.</span></span>

> [!NOTE]
> <span data-ttu-id="3db13-247">Access 2007 (.accdb) データベースの場合、パスワードは暗号化キーです。</span><span class="sxs-lookup"><span data-stu-id="3db13-247">For Access 2007 (.accdb) databases, the password is the encryption key</span></span>

<span data-ttu-id="3db13-248">コマンド ボタンには、次のサンプル VBA コードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3db13-248">You can use the following example VBA code for a command button:</span></span>

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

<span data-ttu-id="3db13-249">次のコードサンプルは、パスワード（暗号化キー）を指定してCompactDatabaseを使用し、その圧縮データベース内のテーブルにリンクする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3db13-249">The following code sample shows how to use CompactDatabase with a password (encryption key) and then link to a table in that compacted database.</span></span> <span data-ttu-id="3db13-250">パスワードを付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3db13-250">Note that a password must be supplied.</span></span>

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
