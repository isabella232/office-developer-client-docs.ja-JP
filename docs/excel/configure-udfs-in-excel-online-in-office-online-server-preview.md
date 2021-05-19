---
title: '[オンライン] で UDF Excelを構成Office Online Server'
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: カスタム関数を呼び出す場合は、Excelのユーザー Office Online Server関数 (UDF) を使用します。
ms.openlocfilehash: e1b005079c03ae3028ba6bf9ee1156c6ae2eae80
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102934"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="cff95-103">[オンライン] で UDF Excelを構成Office Online Server</span><span class="sxs-lookup"><span data-stu-id="cff95-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="cff95-104">カスタム関数を呼び出す場合は、Excelのユーザー Office Online Server関数 (UDF) を使用します。</span><span class="sxs-lookup"><span data-stu-id="cff95-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="cff95-p101">Excel Online でユーザー定義関数 (UDF) を使用すると、セル内の数式を使用して、マネージ コードで記述されたカスタム関数を呼び出すことができます。UDF は、次の目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="cff95-p101">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells. You can use UDFs to:</span></span>
  
- <span data-ttu-id="cff95-107">カスタムの数学関数を呼び出す</span><span class="sxs-lookup"><span data-stu-id="cff95-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="cff95-108">カスタム データ ソースからデータを取得してワークシートに入力する</span><span class="sxs-lookup"><span data-stu-id="cff95-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="cff95-109">Web サービスを呼び出す</span><span class="sxs-lookup"><span data-stu-id="cff95-109">Call web services.</span></span>
    
<span data-ttu-id="cff95-110">UDF バイナリは、以下の 2 つの場所のいずれかにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="cff95-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="cff95-p102">ローカル ディレクトリ。例:</span><span class="sxs-lookup"><span data-stu-id="cff95-p102">A local directory. For example:</span></span> 
    
    <span data-ttu-id="cff95-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="cff95-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="cff95-p103">グローバル アセンブリ キャッシュ。例:</span><span class="sxs-lookup"><span data-stu-id="cff95-p103">The global assembly cache. For example:</span></span> 
    
    <span data-ttu-id="cff95-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="cff95-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="cff95-117">新しい **OfficeWebAppsExcelUserDefinedFunction** 定義を作成するときに場所を参照Office Online Server。</span><span class="sxs-lookup"><span data-stu-id="cff95-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cff95-118">Office Online Server共有上にある UDF はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="cff95-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="cff95-119">デバイスで UDF を有効Office Online Server</span><span class="sxs-lookup"><span data-stu-id="cff95-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="cff95-120">管理者が[New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps)コマンドレットOfficeして Web Apps Server ファームに新しいアプリケーション をWindows PowerShellすると、UDF アセンブリは既定で無効になっています。</span><span class="sxs-lookup"><span data-stu-id="cff95-120">When an administrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="cff95-121">**ExcelUdfsAllowed** フラグの既定値は false です。</span><span class="sxs-lookup"><span data-stu-id="cff95-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="cff95-122">UDF を有効にするには、Web Apps サーバー ファームWindows PowerShellした後、Office Online Serverで次Officeコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="cff95-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="cff95-123">UDF 定義を作成するOffice Online Server</span><span class="sxs-lookup"><span data-stu-id="cff95-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="cff95-124">UDF を有効にした後に、UDF を含むバイナリの定義を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cff95-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="cff95-125">UDF バイナリの定義を作成するには、Office Online Server **New-OfficeWebAppsExcelUserDefinedFunction コマンドレットを使用** します。</span><span class="sxs-lookup"><span data-stu-id="cff95-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="cff95-126">このコマンドレットには、次のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="cff95-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="cff95-127">**アセンブリ**</span><span class="sxs-lookup"><span data-stu-id="cff95-127">**Assembly**</span></span>
    
- <span data-ttu-id="cff95-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="cff95-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="cff95-129">**Enable** (既定で False に設定されます)</span><span class="sxs-lookup"><span data-stu-id="cff95-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="cff95-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="cff95-130">**Description**</span></span>
    
<span data-ttu-id="cff95-131">次の例は、UDF 定義を作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cff95-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="cff95-132">新しい UDF 参照を作成した後、サーバーで **iisreset** を実行して、その参照をすぐに選択します。</span><span class="sxs-lookup"><span data-stu-id="cff95-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="cff95-133">UDF Office Online ServerコマンドWindows PowerShell追加</span><span class="sxs-lookup"><span data-stu-id="cff95-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="cff95-134">UDF を使用するにはWindows PowerShellのコマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="cff95-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="cff95-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (必須パラメーターなし) - アプリケーションで構成されている UDF 定義の一覧をOffice Online Server。</span><span class="sxs-lookup"><span data-stu-id="cff95-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="cff95-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義にプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="cff95-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="cff95-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義を削除します。</span><span class="sxs-lookup"><span data-stu-id="cff95-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="cff95-138">UDF のサンプル</span><span class="sxs-lookup"><span data-stu-id="cff95-138">UDF sample</span></span>

<span data-ttu-id="cff95-139">次のサンプル ファイルは、UDF と UDF バイナリを使用するサンプル ブックを提供します。</span><span class="sxs-lookup"><span data-stu-id="cff95-139">The following sample file provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="cff95-140">[BooleanDataType.xlsx: ](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx)UDF を使用するサンプル ブック</span><span class="sxs-lookup"><span data-stu-id="cff95-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="cff95-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="cff95-141">See also</span></span>

- [<span data-ttu-id="cff95-142">Excel Online の管理設定を行う</span><span class="sxs-lookup"><span data-stu-id="cff95-142">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="cff95-143">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="cff95-143">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

