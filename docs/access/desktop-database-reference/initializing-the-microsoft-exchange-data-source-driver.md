---
title: Microsoft Exchange データ ソース ドライバーを初期化しています。
TOCTitle: Initializing the Microsoft Exchange Data Source driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 39cad98bc6f14509491e78ac4057d6488528f0b4
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947855"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a><span data-ttu-id="9427e-102">Microsoft Exchange データ ソース ドライバーを初期化しています。</span><span class="sxs-lookup"><span data-stu-id="9427e-102">Initializing the Microsoft Exchange Data Source driver</span></span>

<span data-ttu-id="9427e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9427e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9427e-104">Microsoft Exchange データ ソース ドライバーをインストールすると、セットアップ プログラムは、一連の既定値をエンジンと ISAM 形式のサブキーで、Microsoft Windows レジストリに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="9427e-104">When you install the Microsoft Exchange Data Source driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="9427e-105">これらの設定を直接変更しないでください。追加、削除、またはこれらの設定を変更するには、アプリケーションのセットアップ プログラムを使用します。</span><span class="sxs-lookup"><span data-stu-id="9427e-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="9427e-106">次のセクションでは、初期設定と Microsoft Exchange データ ソース ドライバーの ISAM 形式の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="9427e-106">The following sections describe initialization and ISAM Format settings for the Microsoft Exchange Data Source driver.</span></span>

## <a name="microsoft-exchange-data-source-initialization-settings"></a><span data-ttu-id="9427e-107">Microsoft Exchange データ ソースの初期設定</span><span class="sxs-lookup"><span data-stu-id="9427e-107">Microsoft Exchange Data Source Initialization Settings</span></span>

<span data-ttu-id="9427e-108">**アクセス接続エンジン\\エンジン\\Exchange**フォルダーには、Aceexch.dll ドライバーは、Microsoft Outlook と Microsoft Exchange フォルダーへの外部アクセスのための初期設定が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9427e-108">The **Access Connectivity Engine\\Engines\\Exchange** folder includes initialization settings for the Aceexch.dll driver, used for external access to Microsoft Outlook and Microsoft Exchange folders.</span></span> <span data-ttu-id="9427e-109">このキーのエントリは 1 つだけで、その設定は次のようになっています。</span><span class="sxs-lookup"><span data-stu-id="9427e-109">The only entry in this folder is the following:</span></span>

`win32=<path>\ACEEXCH.DLL`

<span data-ttu-id="9427e-110">Microsoft Access データベース エンジンは、この設定を使用して Aceexch.dll の格納場所を示します。</span><span class="sxs-lookup"><span data-stu-id="9427e-110">The Microsoft Access database engine uses this setting to indicate the location of Aceexch.dll.</span></span> <span data-ttu-id="9427e-111">このフル パスはインストール時に決まります。</span><span class="sxs-lookup"><span data-stu-id="9427e-111">The full path is determined at the time of installation.</span></span> <span data-ttu-id="9427e-112">REG の型の値は、\_SZ です。</span><span class="sxs-lookup"><span data-stu-id="9427e-112">Values are of type REG\_SZ.</span></span>

<span data-ttu-id="9427e-p104">Microsoft Outlook の ISAM 形式の使用結果と Microsoft Exchange クライアントの ISAM 形式の使用結果は似ています。唯一の違いは、異なる 2 つのクライアントが、同じ列に異なる名前を使用することです。2 つの ISAM 形式は、Microsoft Access データベース エンジンがユーザーの望む特定のスタイルで列名を返すことができるように作られています。</span><span class="sxs-lookup"><span data-stu-id="9427e-p104">The results of using the Outlook ISAM format and of using the Exchange client ISAM format are similar. The only difference is that the two different clients use different names for the same columns. The two ISAM formats have been created so that the Microsoft Access database engine can return the column names in the particular style that the user desires.</span></span>

## <a name="microsoft-outlook-client-isam-formats"></a><span data-ttu-id="9427e-116">Microsoft Outlook クライアントの ISAM 形式</span><span class="sxs-lookup"><span data-stu-id="9427e-116">Microsoft Outlook Client ISAM Formats</span></span>

<span data-ttu-id="9427e-117">**アクセス接続エンジン\\ISAM 形式\\Outlook 9.0**フォルダーには、次のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9427e-117">The **Access Connectivity Engine\\ISAM Formats\\Outlook 9.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9427e-118">エントリ名</span><span class="sxs-lookup"><span data-stu-id="9427e-118">Entry name</span></span></p></th>
<th><p><span data-ttu-id="9427e-119">型</span><span class="sxs-lookup"><span data-stu-id="9427e-119">Type</span></span></p></th>
<th><p><span data-ttu-id="9427e-120">値</span><span class="sxs-lookup"><span data-stu-id="9427e-120">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9427e-121">Engine</span><span class="sxs-lookup"><span data-stu-id="9427e-121">Engine</span></span></p></td>
<td><p><span data-ttu-id="9427e-122">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9427e-122">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9427e-123">Exchange</span><span class="sxs-lookup"><span data-stu-id="9427e-123">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9427e-124">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="9427e-124">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="9427e-125">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9427e-125">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9427e-126">Outlook()</span><span class="sxs-lookup"><span data-stu-id="9427e-126">Outlook()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9427e-127">CanLink</span><span class="sxs-lookup"><span data-stu-id="9427e-127">CanLink</span></span></p></td>
<td><p><span data-ttu-id="9427e-128">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9427e-128">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9427e-129">01</span><span class="sxs-lookup"><span data-stu-id="9427e-129">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9427e-130">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="9427e-130">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="9427e-131">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9427e-131">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9427e-132">00</span><span class="sxs-lookup"><span data-stu-id="9427e-132">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9427e-133">IsamType</span><span class="sxs-lookup"><span data-stu-id="9427e-133">IsamType</span></span></p></td>
<td><p><span data-ttu-id="9427e-134">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="9427e-134">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="9427e-135">3</span><span class="sxs-lookup"><span data-stu-id="9427e-135">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9427e-136">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="9427e-136">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="9427e-137">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9427e-137">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9427e-138">00</span><span class="sxs-lookup"><span data-stu-id="9427e-138">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9427e-139">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="9427e-139">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="9427e-140">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9427e-140">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9427e-141">00</span><span class="sxs-lookup"><span data-stu-id="9427e-141">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9427e-142">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="9427e-142">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="9427e-143">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9427e-143">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9427e-144">01</span><span class="sxs-lookup"><span data-stu-id="9427e-144">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="9427e-145">[!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9427e-145">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="microsoft-exchange-client-isam-formats"></a><span data-ttu-id="9427e-146">Microsoft Exchange クライアントの ISAM 形式</span><span class="sxs-lookup"><span data-stu-id="9427e-146">Microsoft Exchange Client ISAM Formats</span></span>

<span data-ttu-id="9427e-147">**アクセス接続エンジン\\ISAM 形式\\Exchange 4.0**フォルダーには、次のエントリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9427e-147">The **Access Connectivity Engine\\ISAM Formats\\Exchange 4.0** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9427e-148">エントリ名</span><span class="sxs-lookup"><span data-stu-id="9427e-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="9427e-149">型</span><span class="sxs-lookup"><span data-stu-id="9427e-149">Type</span></span></p></th>
<th><p><span data-ttu-id="9427e-150">値</span><span class="sxs-lookup"><span data-stu-id="9427e-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9427e-151">Engine</span><span class="sxs-lookup"><span data-stu-id="9427e-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="9427e-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9427e-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9427e-153">Exchange</span><span class="sxs-lookup"><span data-stu-id="9427e-153">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9427e-154">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="9427e-154">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="9427e-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="9427e-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="9427e-156">Exchange()</span><span class="sxs-lookup"><span data-stu-id="9427e-156">Exchange()</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9427e-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="9427e-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="9427e-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9427e-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9427e-159">01</span><span class="sxs-lookup"><span data-stu-id="9427e-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9427e-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="9427e-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="9427e-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9427e-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9427e-162">00</span><span class="sxs-lookup"><span data-stu-id="9427e-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9427e-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="9427e-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="9427e-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="9427e-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="9427e-165">3</span><span class="sxs-lookup"><span data-stu-id="9427e-165">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9427e-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="9427e-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="9427e-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9427e-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9427e-168">00</span><span class="sxs-lookup"><span data-stu-id="9427e-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9427e-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="9427e-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="9427e-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9427e-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9427e-171">00</span><span class="sxs-lookup"><span data-stu-id="9427e-171">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9427e-172">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="9427e-172">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="9427e-173">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="9427e-173">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="9427e-174">01</span><span class="sxs-lookup"><span data-stu-id="9427e-174">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="9427e-175">[!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9427e-175">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a><span data-ttu-id="9427e-176">Microsoft Outlook データと Microsoft Exchange データのために Schema.ini ファイルをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="9427e-176">Customizing the Schema.ini File for Outlook and Exchange Data</span></span>

<span data-ttu-id="9427e-p105">Schema.ini ファイルは、テキストの ISAM で使用されるのと同様の方法で、Microsoft Outlook と Microsoft Exchange の ISAM でも使用されます。Schema.ini には、データの書式化方法、アクセスされる列名など、データ ソースの仕様が記述されています。</span><span class="sxs-lookup"><span data-stu-id="9427e-p105">The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini contains the specifics of a data source: how the data is formatted, and the names of columns that should be accessed.</span></span>

<span data-ttu-id="9427e-p106">Outlook や Exchange で、データの読み込み、インポート、またはエクスポートを行う前に、Schema.ini ファイルを変更する必要はありません。Outlook と Exchange のための Schema.ini ファイル内の設定の多くは、MAPI が必要とする内部タグに特有のものです。これらのタグの値は変更しないでください。</span><span class="sxs-lookup"><span data-stu-id="9427e-p106">It is not necessary to modify the Schema.ini file before data can be read, imported, or exported for Outlook and Exchange. Many of the settings inside the Schema.ini file for Outlook and Exchange are specific to internal tags that MAPI requires. You should not attempt to modify those tag values.</span></span>

