---
title: Microsoft Exchange データ ソース ドライバーを初期化する
TOCTitle: Initializing the Microsoft Exchange Data Source Driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f711e9814e32742c89c37ae3357111143ca18b6e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476300"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="13cb2-102">Microsoft Exchange データ ソース ドライバーを初期化する</span><span class="sxs-lookup"><span data-stu-id="13cb2-102">Initializing the Microsoft Exchange Data Source Driver</span></span>

<span data-ttu-id="13cb2-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="13cb2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="13cb2-p101">Microsoft® Exchange データ ソース ドライバーをインストールすると、セットアップ プログラムは Microsoft Windows® レジストリの Engines サブキーと ISAM Formats サブキーに一連の既定値を書き込みます。これらの設定は直接変更しないでください。これらの設定に対して追加、削除、変更を行う場合は、アプリケーションのセットアップ プログラムを使用します。Microsoft Exchange データ ソース ドライバーの初期設定と ISAM 形式の設定に関する説明を、次に示します。</span><span class="sxs-lookup"><span data-stu-id="13cb2-p101">When you install the Microsoft® Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows® Registry in the Engines and ISAM Formats subkeys. You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings. The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="13cb2-107">Microsoft Exchange データ ソースの初期設定</span><span class="sxs-lookup"><span data-stu-id="13cb2-107">Microsoft Exchange Data Source Initialization Settings</span></span>

<span data-ttu-id="13cb2-108">**アクセス接続エンジン\\エンジン\\Exchange**フォルダーには、Aceexch.dll ドライバーは、Microsoft Outlook と Microsoft Exchange フォルダーへの外部アクセスのための初期設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="13cb2-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="13cb2-109">このキーのエントリは 1 つだけで、その設定は次のようになっています。</span><span class="sxs-lookup"><span data-stu-id="13cb2-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="13cb2-110">Microsoft Access データベース エンジンは、この設定を使用して Aceexch.dll の格納場所を示します。</span><span class="sxs-lookup"><span data-stu-id="13cb2-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="13cb2-111">このフル パスはインストール時に決まります。</span><span class="sxs-lookup"><span data-stu-id="13cb2-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="13cb2-112">REG の型の値は、\_SZ です。</span><span class="sxs-lookup"><span data-stu-id="13cb2-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="13cb2-p104">Microsoft Outlook の ISAM 形式の使用結果と Microsoft Exchange クライアントの ISAM 形式の使用結果は似ています。唯一の違いは、異なる 2 つのクライアントが、同じ列に異なる名前を使用することです。2 つの ISAM 形式は、Microsoft Access データベース エンジンがユーザーの望む特定のスタイルで列名を返すことができるように作られています。</span><span class="sxs-lookup"><span data-stu-id="13cb2-p104">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar. The only difference is that the two different clients use different names for the same columns. The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="13cb2-116">Microsoft Outlook クライアントの ISAM 形式</span><span class="sxs-lookup"><span data-stu-id="13cb2-116">Microsoft Outlook Client ISAM Formats</span></span>

<span data-ttu-id="13cb2-117">**アクセス接続エンジン\\ISAM 形式\\Outlook 9.0**フォルダーには、次のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="13cb2-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13cb2-118">エントリ名</span><span class="sxs-lookup"><span data-stu-id="13cb2-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="13cb2-119">種類</span><span class="sxs-lookup"><span data-stu-id="13cb2-119">Type</span></span></p></th>
<th><p><span data-ttu-id="13cb2-120">値</span><span class="sxs-lookup"><span data-stu-id="13cb2-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13cb2-121">Engine</span><span class="sxs-lookup"><span data-stu-id="13cb2-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="13cb2-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="13cb2-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="13cb2-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="13cb2-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13cb2-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="13cb2-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="13cb2-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="13cb2-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="13cb2-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="13cb2-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13cb2-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="13cb2-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="13cb2-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13cb2-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13cb2-129">01</span><span class="sxs-lookup"><span data-stu-id="13cb2-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13cb2-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="13cb2-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="13cb2-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13cb2-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13cb2-132">00</span><span class="sxs-lookup"><span data-stu-id="13cb2-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13cb2-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="13cb2-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="13cb2-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="13cb2-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="13cb2-135">3</span><span class="sxs-lookup"><span data-stu-id="13cb2-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13cb2-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="13cb2-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="13cb2-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13cb2-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13cb2-138">00</span><span class="sxs-lookup"><span data-stu-id="13cb2-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13cb2-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="13cb2-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="13cb2-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13cb2-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13cb2-141">00</span><span class="sxs-lookup"><span data-stu-id="13cb2-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13cb2-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="13cb2-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="13cb2-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13cb2-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13cb2-144">01</span><span class="sxs-lookup"><span data-stu-id="13cb2-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="13cb2-145">[!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13cb2-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="13cb2-146">Microsoft Exchange クライアントの ISAM 形式</span><span class="sxs-lookup"><span data-stu-id="13cb2-146">Microsoft Exchange Client ISAM Formats</span></span>

<span data-ttu-id="13cb2-147">**アクセス接続エンジン\\ISAM 形式\\Exchange 4.0**フォルダーには、次のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="13cb2-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="13cb2-148">エントリ名</span><span class="sxs-lookup"><span data-stu-id="13cb2-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="13cb2-149">種類</span><span class="sxs-lookup"><span data-stu-id="13cb2-149">Type</span></span></p></th>
<th><p><span data-ttu-id="13cb2-150">値</span><span class="sxs-lookup"><span data-stu-id="13cb2-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13cb2-151">Engine</span><span class="sxs-lookup"><span data-stu-id="13cb2-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="13cb2-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="13cb2-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="13cb2-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="13cb2-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13cb2-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="13cb2-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="13cb2-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="13cb2-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="13cb2-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="13cb2-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13cb2-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="13cb2-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="13cb2-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13cb2-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13cb2-159">01</span><span class="sxs-lookup"><span data-stu-id="13cb2-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13cb2-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="13cb2-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="13cb2-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13cb2-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13cb2-162">00</span><span class="sxs-lookup"><span data-stu-id="13cb2-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13cb2-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="13cb2-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="13cb2-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="13cb2-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="13cb2-165">3</span><span class="sxs-lookup"><span data-stu-id="13cb2-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13cb2-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="13cb2-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="13cb2-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13cb2-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13cb2-168">00</span><span class="sxs-lookup"><span data-stu-id="13cb2-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13cb2-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="13cb2-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="13cb2-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13cb2-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13cb2-171">00</span><span class="sxs-lookup"><span data-stu-id="13cb2-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13cb2-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="13cb2-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="13cb2-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="13cb2-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="13cb2-174">01</span><span class="sxs-lookup"><span data-stu-id="13cb2-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="13cb2-175">[!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13cb2-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="13cb2-176">Microsoft Outlook データと Microsoft Exchange データのために Schema.ini ファイルをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="13cb2-176">Customizing the Schema.ini File for Outlook and Exchange Data</span></span>

<span data-ttu-id="13cb2-p105">Schema.ini ファイルは、テキストの ISAM で使用されるのと同様の方法で、Microsoft Outlook と Microsoft Exchange の ISAM でも使用されます。Schema.ini には、データの書式化方法、アクセスされる列名など、データ ソースの仕様が記述されています。</span><span class="sxs-lookup"><span data-stu-id="13cb2-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="13cb2-p106">Outlook や Exchange で、データの読み込み、インポート、またはエクスポートを行う前に、Schema.ini ファイルを変更する必要はありません。Outlook と Exchange のための Schema.ini ファイル内の設定の多くは、MAPI が必要とする内部タグに特有のものです。これらのタグの値は変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="13cb2-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span></span>

