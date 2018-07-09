---
title: Office Online Server プレビューの Excel Online での UDF の構成
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: カスタム関数を呼び出すには、Office オンライン サーバーのプレビューで Excel のオンラインでユーザー定義関数 (Udf) を使用します。
ms.openlocfilehash: ae2d668ebd4a4df278a5c19e702de248b1749b84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798759"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server-preview"></a><span data-ttu-id="6c177-103">Office Online Server プレビューの Excel Online での UDF の構成</span><span class="sxs-lookup"><span data-stu-id="6c177-103">Configure UDFs in Excel Online in Office Online Server Preview</span></span>

<span data-ttu-id="6c177-104">[このトピックはプレリリース版のドキュメントし、将来のリリースで変更されることは]。カスタム関数を呼び出すには、Office オンライン サーバーのプレビューで Excel のオンラインでユーザー定義関数 (Udf) を使用します。</span><span class="sxs-lookup"><span data-stu-id="6c177-104">[This topic is pre-release documentation and is subject to change in future releases.] Use user-defined functions (UDFs) in Excel Online in Office Online Server Preview to call custom functions.</span></span> 
  
<span data-ttu-id="6c177-p101">Excel Online でユーザー定義関数 (UDF) を使用すると、セル内の数式を使用して、マネージ コードで記述されたカスタム関数を呼び出すことができます。UDF は、次の目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="6c177-p101">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells. You can use UDFs to:</span></span>
  
- <span data-ttu-id="6c177-107">カスタムの数学関数を呼び出す</span><span class="sxs-lookup"><span data-stu-id="6c177-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="6c177-108">カスタム データ ソースからデータを取得してワークシートに入力する</span><span class="sxs-lookup"><span data-stu-id="6c177-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="6c177-109">Web サービスを呼び出す</span><span class="sxs-lookup"><span data-stu-id="6c177-109">Call web services.</span></span>
    
<span data-ttu-id="6c177-110">UDF バイナリは、以下の 2 つの場所のいずれかにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="6c177-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="6c177-p102">ローカル ディレクトリ。例:</span><span class="sxs-lookup"><span data-stu-id="6c177-p102">A local directory. For example:</span></span> 
    
    <span data-ttu-id="6c177-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="6c177-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="6c177-p103">グローバル アセンブリ キャッシュ。例:</span><span class="sxs-lookup"><span data-stu-id="6c177-p103">The global assembly cache. For example:</span></span> 
    
    <span data-ttu-id="6c177-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="6c177-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="6c177-117">Office オンライン サーバー プレビューの**新しい OfficeWebAppsExcelUserDefinedFunction**の定義を作成するときは、場所を参照します。</span><span class="sxs-lookup"><span data-stu-id="6c177-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server Preview.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6c177-118">Office オンライン サーバーのプレビューでは、ネットワーク共有上に配置する Udf をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="6c177-118">Office Online Server Preview does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server-preview"></a><span data-ttu-id="6c177-119">Office オンラインのサーバーのプレビューでは、ユーザー定義関数を有効にします。</span><span class="sxs-lookup"><span data-stu-id="6c177-119">Enable UDFs on Office Online Server Preview</span></span>

<span data-ttu-id="6c177-120">[新規 OfficeWebAppsFarm](https://technet.microsoft.com/ja-jp/library/jj219436.aspx)の Windows PowerShell コマンドレットを使用して、管理者が新しい Office Web アプリケーションのサーバー ファームを作成すると、UDF アセンブリは、既定で無効になります。</span><span class="sxs-lookup"><span data-stu-id="6c177-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/ja-jp/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="6c177-121">**ExcelUdfsAllowed**フラグの既定値は、false を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c177-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="6c177-122">Udf を有効にするには、Office Web アプリケーションのサーバー ファームを作成した後、Office オンライン サーバーのプレビューで次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="6c177-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server Preview, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server-preview"></a><span data-ttu-id="6c177-123">Office オンライン サーバーのプレビューでの UDF の定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="6c177-123">Create UDF definitions on Office Online Server Preview</span></span>

<span data-ttu-id="6c177-124">Udf を有効にした後、ユーザー定義関数が含まれているバイナリの定義を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c177-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="6c177-125">バイナリ Office オンライン サーバーのプレビューで、UDF の定義を作成するには、**新規 OfficeWebAppsExcelUserDefinedFunction**コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="6c177-125">To create a definition for your UDF binary on the Office Online Server Preview, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="6c177-126">このコマンドレットには、次のパラメーターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6c177-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="6c177-127">**アセンブリ**</span><span class="sxs-lookup"><span data-stu-id="6c177-127">**Assembly**</span></span>
    
- <span data-ttu-id="6c177-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="6c177-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="6c177-129">**有効にします。**(既定では、False に設定)</span><span class="sxs-lookup"><span data-stu-id="6c177-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="6c177-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="6c177-130">**Description**</span></span>
    
<span data-ttu-id="6c177-131">次の例は、UDF 定義を作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6c177-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="6c177-132">新しい UDF 参照を作成した後は、すぐに参照を選択するのにはサーバー上で**iisreset**を実行します。</span><span class="sxs-lookup"><span data-stu-id="6c177-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-preview-udf-windows-powershell-commands"></a><span data-ttu-id="6c177-133">Office オンライン サーバー プレビュー UDF Windows PowerShell コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="6c177-133">Additional Office Online Server Preview UDF Windows PowerShell commands</span></span>

<span data-ttu-id="6c177-134">Udf を使用するには、次の Windows PowerShell コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="6c177-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="6c177-135">**Get OfficeWebAppsExcelUserDefinedFunction**(必要なパラメーターなし) の Office オンライン サーバーのプレビューに設定されている UDF の定義の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="6c177-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server Preview.</span></span> 
    
- <span data-ttu-id="6c177-136">**セット OfficeWebAppsExcelUserDefinedFunction**(Identity パラメーターが必要) では、既存の UDF の定義にプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="6c177-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="6c177-137">**削除 OfficeWebAppsExcelUserDefinedFunction**(Identity パラメーターが必要) では、既存の UDF の定義を削除します。</span><span class="sxs-lookup"><span data-stu-id="6c177-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="6c177-138">UDF のサンプル</span><span class="sxs-lookup"><span data-stu-id="6c177-138">UDF sample</span></span>

<span data-ttu-id="6c177-139">次のファイルは、UDF と UDF バイナリを使用するサンプルのブックを提供します。</span><span class="sxs-lookup"><span data-stu-id="6c177-139">The following files provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="6c177-140">[BooleanDataType.xlsx](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) - UDF を使用するサンプル ブック</span><span class="sxs-lookup"><span data-stu-id="6c177-140">[BooleanDataType.xlsx](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) -- a sample workbook that uses a UDF</span></span>  
- <span data-ttu-id="6c177-141">[EcsUdfsCommonSet.dll](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/EcsUdfsCommonSet.dll) - UDF バイナリ</span><span class="sxs-lookup"><span data-stu-id="6c177-141">[EcsUdfsCommonSet.dll](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/EcsUdfsCommonSet.dll) -- the UDF binary</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="6c177-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c177-142">See also</span></span>

- [<span data-ttu-id="6c177-143">Excel のオンライン管理の設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="6c177-143">Configure Excel Online administrative settings</span></span>](https://technet.microsoft.com/ja-jp/library/jj219698%28v=office.16%29.aspx)  
- [<span data-ttu-id="6c177-144">Office オンラインのサーバーのプレビュー</span><span class="sxs-lookup"><span data-stu-id="6c177-144">Office Online Server Preview</span></span>](https://technet.microsoft.com/ja-jp/library/jj219456%28v=office.16%29.aspx)
    

