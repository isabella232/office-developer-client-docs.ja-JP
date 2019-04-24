---
title: CreateDatabase メソッド (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6d271676ef91d29dca78ba9ee4b6142e055b36d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305867"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="462b6-102">CreateDatabase メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="462b6-102">Workspace.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="462b6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="462b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="462b6-104">新しい **[Database](database-object-dao.md)** オブジェクトを作成し、そのデータベースをディスクに保存し、開かれた **Database** オブジェクトとして返します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="462b6-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="462b6-105">構文</span><span class="sxs-lookup"><span data-stu-id="462b6-105">Syntax</span></span>

<span data-ttu-id="462b6-106">*式*。CreateDatabase (***名前***、***接続***、***オプション***)</span><span class="sxs-lookup"><span data-stu-id="462b6-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="462b6-107">\*式\***Workspace**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="462b6-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="462b6-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="462b6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="462b6-109">名前</span><span class="sxs-lookup"><span data-stu-id="462b6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="462b6-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="462b6-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="462b6-111">データ型</span><span class="sxs-lookup"><span data-stu-id="462b6-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="462b6-112">説明</span><span class="sxs-lookup"><span data-stu-id="462b6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="462b6-113"><em>名前</em></span><span class="sxs-lookup"><span data-stu-id="462b6-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="462b6-114">必須</span><span class="sxs-lookup"><span data-stu-id="462b6-114">Required</span></span></p></td>
<td><p><span data-ttu-id="462b6-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-116">A String up to 255 characters long that is the name of the database file that you're creating.</span><span class="sxs-lookup"><span data-stu-id="462b6-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="462b6-117">It can be the full path and file name.</span><span class="sxs-lookup"><span data-stu-id="462b6-117">It can be the full path and file name.</span></span> <span data-ttu-id="462b6-118">ネットワークでサポートされている場合は、server1\share1\dir1\db1 &quot; \\&quot;などのネットワークパスを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="462b6-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="462b6-119">You can only create Microsoft Access database files with this method.</span><span class="sxs-lookup"><span data-stu-id="462b6-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-120"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="462b6-120"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="462b6-121">必須</span><span class="sxs-lookup"><span data-stu-id="462b6-121">Required</span></span></p></td>
<td><p><span data-ttu-id="462b6-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="462b6-p102">[設定] で指定された、データベースを作成する際の照合順序を表す文字列式。この引数を指定しないと、エラーが発生します。  </span><span class="sxs-lookup"><span data-stu-id="462b6-p102">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="462b6-125">次に示すように、 <em>locale</em>引数の<strong></strong>定数に、(;p wd = &quot;&quot;で始まる) パスワード文字列を連結することによって、新しい Database オブジェクトのパスワードを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="462b6-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="462b6-126">dblangspanish &amp; &quot;語;p wd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="462b6-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="462b6-127">既定の <em>locale</em> を使用し、パスワードを指定する場合は、単に <em>locale</em> 引数としてパスワード文字列を入力します。</span><span class="sxs-lookup"><span data-stu-id="462b6-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="462b6-128">&quot;;p wd = NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="462b6-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="462b6-p103">大文字、小文字、数字、記号を組み合わせた強力なパスワードを使用してください。これらの文字を混在させていないパスワードは脆弱なパスワードです。Y6dh!et5 は強力なパスワードです。House27 は脆弱なパスワードです。強力なパスワードでありながら、書き留めておかなくても覚えておくことができるパスワードを使用してください。  </span><span class="sxs-lookup"><span data-stu-id="462b6-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-134"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="462b6-134"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="462b6-135">Optional</span><span class="sxs-lookup"><span data-stu-id="462b6-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="462b6-136"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-p104">1 つ以上のオプションを示す定数 (または定数の組み合わせ)。オプションを組み合わせるには、対応する定数を追加します。</span><span class="sxs-lookup"><span data-stu-id="462b6-p104">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="462b6-139">注釈</span><span class="sxs-lookup"><span data-stu-id="462b6-139">Remarks</span></span>

<span data-ttu-id="462b6-140">次の定数のいずれかを引数 locale に使用して、文字列比較を行うテキストの [CollatingOrder](database-collatingorder-property-dao.md) プロパティを指定できます。</span><span class="sxs-lookup"><span data-stu-id="462b6-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="462b6-141">定数</span><span class="sxs-lookup"><span data-stu-id="462b6-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="462b6-142">照合順序</span><span class="sxs-lookup"><span data-stu-id="462b6-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="462b6-143"><strong>dblanggeneral</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-144">英語、ドイツ語、フランス語、ポルトガル語、イタリア語、現代スペイン語</span><span class="sxs-lookup"><span data-stu-id="462b6-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-145"><strong>dblangarabic 語</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-146">アラビア語</span><span class="sxs-lookup"><span data-stu-id="462b6-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-147"><strong>dblangchinesesimplified</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-148">簡体字中国語</span><span class="sxs-lookup"><span data-stu-id="462b6-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-149"><strong>dblangchinesetraditional</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-150">繁体字中国語</span><span class="sxs-lookup"><span data-stu-id="462b6-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-151"><strong>dblangcyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-152">ロシア語</span><span class="sxs-lookup"><span data-stu-id="462b6-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-153"><strong>dblangczech</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-154">チェコ語</span><span class="sxs-lookup"><span data-stu-id="462b6-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-155"><strong>dblangdutch 語</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-156">オランダ語</span><span class="sxs-lookup"><span data-stu-id="462b6-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-157"><strong>dblanggreek 語</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-158">ギリシャ語</span><span class="sxs-lookup"><span data-stu-id="462b6-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-159"><strong>dblanghebrew 語</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-160">ヘブライ語</span><span class="sxs-lookup"><span data-stu-id="462b6-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-161"><strong>dblanghungarian</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-162">ハンガリー語</span><span class="sxs-lookup"><span data-stu-id="462b6-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-163"><strong>dblangicelandic 語</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-164">アイスランド語</span><span class="sxs-lookup"><span data-stu-id="462b6-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-165"><strong>dblangjapanese</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-166">日本語</span><span class="sxs-lookup"><span data-stu-id="462b6-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-167"><strong>dblangkorean 語</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-168">韓国語</span><span class="sxs-lookup"><span data-stu-id="462b6-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-169"><strong>dblangnordic</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-170">北欧諸国語 (Microsoft Jet データベース エンジン バージョン 1.0 のみ)</span><span class="sxs-lookup"><span data-stu-id="462b6-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-171"><strong>dblangnorwdan</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-172">ノルウェー語およびデンマーク語</span><span class="sxs-lookup"><span data-stu-id="462b6-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-173"><strong>dblangpolish</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-174">ポーランド語</span><span class="sxs-lookup"><span data-stu-id="462b6-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-175"><strong>dblangslovenian 語</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-176">スロベニア語</span><span class="sxs-lookup"><span data-stu-id="462b6-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-178">古スペイン語</span><span class="sxs-lookup"><span data-stu-id="462b6-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-180">スウェーデン語およびフィンランド語</span><span class="sxs-lookup"><span data-stu-id="462b6-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-181"><strong>dblangthai 語</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-182">タイ語</span><span class="sxs-lookup"><span data-stu-id="462b6-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-183"><strong>dblangturkish</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-184">トルコ語</span><span class="sxs-lookup"><span data-stu-id="462b6-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="462b6-185">次の定数 (複数可) を options 引数に使用して、データ形式のバージョン、およびデータベースを暗号化するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="462b6-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="462b6-186">定数</span><span class="sxs-lookup"><span data-stu-id="462b6-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="462b6-187">説明</span><span class="sxs-lookup"><span data-stu-id="462b6-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="462b6-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-189">暗号化されたデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="462b6-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-191">Microsoft Jet データベース エンジン バージョン 1.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="462b6-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-193">Microsoft Jet データベース エンジン バージョン 1.1 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="462b6-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-195">Microsoft Jet データベース エンジン バージョン 2.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="462b6-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-197">Microsoft Jet データベース エンジン バージョン 3.0 のファイル形式 (バージョン 3.5 と互換性がある) を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="462b6-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="462b6-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-199">Microsoft Jet データベース エンジン バージョン 4.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="462b6-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="462b6-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="462b6-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="462b6-201">Microsoft Access データベース エンジン バージョン 12.0 のファイル形式を使用するデータベースを作成します。</span><span class="sxs-lookup"><span data-stu-id="462b6-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="462b6-202">暗号化の定数を省略した場合は、 **CreateDatabase** により暗号化されていないデータベースが作成されます。</span><span class="sxs-lookup"><span data-stu-id="462b6-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="462b6-p105">**CreateDatabase** メソッドは、新しい空のデータベースを作成して開き、 **Database** オブジェクトを取得するために使用します。データベースの構造と内容は、別の DAO オブジェクトを使用して指定する必要があります。既存のデータベースの一部または全体をコピーする場合は、 **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** メソッドを使用してカスタマイズ可能なコピーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="462b6-p105">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="462b6-206">例</span><span class="sxs-lookup"><span data-stu-id="462b6-206">Example</span></span>

<span data-ttu-id="462b6-207">次の例では、 **CreateDatabase** メソッドを使用して、新しい暗号化された **Database** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="462b6-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
       Dim wrkDefault As Workspace 
       Dim dbsNew As DATABASE 
       Dim prpLoop As Property 
     
       ' Get default Workspace. 
       Set wrkDefault = DBEngine.Workspaces(0) 
     
       ' Make sure there isn't already a file with the name of  
       ' the new database. 
       If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
       ' Create a new encrypted database with the specified  
       ' collating order. 
       Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
          dbLangGeneral, dbEncrypt) 
     
       With dbsNew 
          Debug.Print "Properties of " & .Name 
          ' Enumerate the Properties collection of the new  
          ' Database object. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
       End With 
     
       dbsNew.Close 
     
    End Sub
```
