---
title: DBEngine.CreateDatabase メソッド (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: d5821a4b-483a-b8fa-e929-5f036057d8c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835033(v=office.15)
ms:contentKeyID: 48547966
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052972
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e988eec4b3997bb24bf3a9aa0bb7faed1629b1f1
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950105"
---
# <a name="dbenginecreatedatabase-method-dao"></a><span data-ttu-id="01151-102">DBEngine.CreateDatabase メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="01151-102">DBEngine.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="01151-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="01151-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="01151-p101">新しい **[Database](database-object-dao.md)** オブジェクトを作成し、そのデータベースをディスクに保存し、開かれた **Database** オブジェクトを取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="01151-p101">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="01151-106">構文</span><span class="sxs-lookup"><span data-stu-id="01151-106">Syntax</span></span>

<span data-ttu-id="01151-107">*式*です。データベース (***名***、***ロケール***、***オプション***)</span><span class="sxs-lookup"><span data-stu-id="01151-107">*expression* .CreateDatabase(***Name***, ***Locale***, ***Option***)</span></span>

<span data-ttu-id="01151-108">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="01151-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="01151-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="01151-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01151-110">名前</span><span class="sxs-lookup"><span data-stu-id="01151-110">Name</span></span></p></th>
<th><p><span data-ttu-id="01151-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="01151-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="01151-112">データ型</span><span class="sxs-lookup"><span data-stu-id="01151-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="01151-113">説明</span><span class="sxs-lookup"><span data-stu-id="01151-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01151-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="01151-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="01151-115">必須</span><span class="sxs-lookup"><span data-stu-id="01151-115">Required</span></span></p></td>
<td><p><span data-ttu-id="01151-116"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="01151-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-117">作成するデータベース ファイルの名前は、255 文字までの文字列です。</span><span class="sxs-lookup"><span data-stu-id="01151-117">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="01151-118">完全なパスとファイル名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="01151-118">It can be the full path and file name.</span></span> <span data-ttu-id="01151-119">ネットワークでサポートされている場合は、指定することもネットワーク パスでは、次のように&quot; \\server1\share1\dir1\db1&quot;。</span><span class="sxs-lookup"><span data-stu-id="01151-119">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="01151-120">のみ、このメソッドを使用して Microsoft Access データベース ファイルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="01151-120">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-121"><em>Locale</em></span><span class="sxs-lookup"><span data-stu-id="01151-121"><em>Locale</em></span></span></p></td>
<td><p><span data-ttu-id="01151-122">必須</span><span class="sxs-lookup"><span data-stu-id="01151-122">Required</span></span></p></td>
<td><p><span data-ttu-id="01151-123"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="01151-123"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="01151-p103">[設定] で指定された、データベースを作成する際の照合順序を表す文字列式。この引数を指定しないと、エラーが発生します。  </span><span class="sxs-lookup"><span data-stu-id="01151-p103">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="01151-126">パスワード文字列を連結して、新しい<strong>Database</strong>オブジェクトのパスワードを作成することもできます (で始まる&quot;; pwd =&quot; ) を次のように、引数<em>locale</em>の定数。</span><span class="sxs-lookup"><span data-stu-id="01151-126">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot; ) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="01151-127">dbLangSpanish &amp; &quot;; pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="01151-127">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="01151-128">既定の <em>locale</em> を使用し、パスワードを指定する場合は、単に <em>locale</em> 引数としてパスワード文字列を入力します。</span><span class="sxs-lookup"><span data-stu-id="01151-128">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="01151-129">&quot;pwd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="01151-129">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="01151-p104">大文字、小文字、数字、記号を組み合わせた強力なパスワードを使用してください。これらの文字を混在させていないパスワードは脆弱なパスワードです。Y6dh!et5 は強力なパスワードです。House27 は脆弱なパスワードです。強力なパスワードでありながら、書き留めておかなくても覚えておくことができるパスワードを使用してください。  </span><span class="sxs-lookup"><span data-stu-id="01151-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-135"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="01151-135"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="01151-136">省略可能</span><span class="sxs-lookup"><span data-stu-id="01151-136">Optional</span></span></p></td>
<td><p><span data-ttu-id="01151-137"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="01151-137"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-p105">1 つ以上のオプションを示す定数 (または定数の組み合わせ)。オプションを組み合わせるには、対応する定数を追加します。</span><span class="sxs-lookup"><span data-stu-id="01151-p105">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="01151-140">解説</span><span class="sxs-lookup"><span data-stu-id="01151-140">Remarks</span></span>

<span data-ttu-id="01151-141">次の定数のいずれかを引数 locale に使用して、文字列比較を行うテキストの **[CollatingOrder](database-collatingorder-property-dao.md)** プロパティを指定できます。</span><span class="sxs-lookup"><span data-stu-id="01151-141">You can use one of the following constants for the locale argument to specify the **[CollatingOrder](database-collatingorder-property-dao.md)** property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01151-142">定数</span><span class="sxs-lookup"><span data-stu-id="01151-142">Constant</span></span></p></th>
<th><p><span data-ttu-id="01151-143">照合順序</span><span class="sxs-lookup"><span data-stu-id="01151-143">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01151-144"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="01151-144"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-145">英語、ドイツ語、フランス語、ポルトガル語、イタリア語、現代スペイン語</span><span class="sxs-lookup"><span data-stu-id="01151-145">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-146"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="01151-146"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-147">アラビア語</span><span class="sxs-lookup"><span data-stu-id="01151-147">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-148"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="01151-148"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-149">簡体字中国語</span><span class="sxs-lookup"><span data-stu-id="01151-149">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-150"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="01151-150"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-151">繁体字中国語</span><span class="sxs-lookup"><span data-stu-id="01151-151">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-152"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="01151-152"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-153">ロシア語</span><span class="sxs-lookup"><span data-stu-id="01151-153">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-154"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="01151-154"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-155">チェコ語</span><span class="sxs-lookup"><span data-stu-id="01151-155">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-156"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="01151-156"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-157">オランダ語</span><span class="sxs-lookup"><span data-stu-id="01151-157">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-158"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="01151-158"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-159">ギリシャ語</span><span class="sxs-lookup"><span data-stu-id="01151-159">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-160"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="01151-160"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-161">ヘブライ語</span><span class="sxs-lookup"><span data-stu-id="01151-161">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-162"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="01151-162"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-163">ハンガリー語</span><span class="sxs-lookup"><span data-stu-id="01151-163">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-164"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="01151-164"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-165">アイスランド語</span><span class="sxs-lookup"><span data-stu-id="01151-165">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-166"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="01151-166"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-167">日本語</span><span class="sxs-lookup"><span data-stu-id="01151-167">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-168"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="01151-168"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-169">韓国語</span><span class="sxs-lookup"><span data-stu-id="01151-169">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-170"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="01151-170"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-171">北欧諸国語 (Microsoft Jet データベース エンジン バージョン 1.0 のみ)</span><span class="sxs-lookup"><span data-stu-id="01151-171">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-172"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="01151-172"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-173">ノルウェー語およびデンマーク語</span><span class="sxs-lookup"><span data-stu-id="01151-173">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-174"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="01151-174"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-175">ポーランド語</span><span class="sxs-lookup"><span data-stu-id="01151-175">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-176"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="01151-176"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-177">スロベニア語</span><span class="sxs-lookup"><span data-stu-id="01151-177">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-178"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="01151-178"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-179">古スペイン語</span><span class="sxs-lookup"><span data-stu-id="01151-179">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-180"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="01151-180"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-181">スウェーデン語およびフィンランド語</span><span class="sxs-lookup"><span data-stu-id="01151-181">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-182"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="01151-182"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-183">タイ語</span><span class="sxs-lookup"><span data-stu-id="01151-183">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-184"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="01151-184"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-185">トルコ語</span><span class="sxs-lookup"><span data-stu-id="01151-185">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="01151-186">次の定数 (複数可) を options 引数に使用して、データ形式のバージョン、およびデータベースを暗号化するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="01151-186">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01151-187">定数</span><span class="sxs-lookup"><span data-stu-id="01151-187">Constant</span></span></p></th>
<th><p><span data-ttu-id="01151-188">説明</span><span class="sxs-lookup"><span data-stu-id="01151-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01151-189"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="01151-189"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-190">暗号化されたデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="01151-190">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-191"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="01151-191"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-192">Microsoft Jet データベース エンジン バージョン 1.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="01151-192">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-193"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="01151-193"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-194">Microsoft Jet データベース エンジン バージョン 1.1 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="01151-194">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-195"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="01151-195"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-196">Microsoft Jet データベース エンジン バージョン 2.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="01151-196">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-197"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="01151-197"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-198">Microsoft Jet データベース エンジン バージョン 3.0 のファイル形式 (バージョン 3.5 と互換性がある) を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="01151-198">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01151-199"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="01151-199"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-200">Microsoft Jet データベース エンジン バージョン 4.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="01151-200">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01151-201"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="01151-201"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="01151-202">Microsoft Access データベース エンジン バージョン 12.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="01151-202">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="01151-203">暗号化の定数を省略した場合は、 **CreateDatabase** により暗号化されていないデータベースが作成されます。</span><span class="sxs-lookup"><span data-stu-id="01151-203">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="01151-p106">**CreateDatabase** メソッドを使用して、新しい空のデータベースを作成して開き、 **Database** オブジェクトを取得します。このオブジェクトの構造と内容は、追加の DAO オブジェクトを使用して完成させる必要があります。既存のデータベースの部分的または完全なコピーを作成する場合は、 **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** メソッドを使用してカスタマイズ可能なコピーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="01151-p106">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

