---
title: Office Online Server の Excel Online で Udf を構成する
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Office Online Server の Excel Online でユーザー定義関数 (Udf) を使用して、カスタム関数を呼び出します。
ms.openlocfilehash: 6e16ea753090b2fefca4ae15330f1a27d53da777
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819358"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="0e87c-103">Office Online Server の Excel Online で Udf を構成する</span><span class="sxs-lookup"><span data-stu-id="0e87c-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="0e87c-104">Office Online Server の Excel Online でユーザー定義関数 (Udf) を使用して、カスタム関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0e87c-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="0e87c-p101">Excel Online でユーザー定義関数 (UDF) を使用すると、セル内の数式を使用して、マネージ コードで記述されたカスタム関数を呼び出すことができます。UDF は、次の目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="0e87c-p101">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells. You can use UDFs to:</span></span>
  
- <span data-ttu-id="0e87c-107">カスタムの数学関数を呼び出す</span><span class="sxs-lookup"><span data-stu-id="0e87c-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="0e87c-108">カスタム データ ソースからデータを取得してワークシートに入力する</span><span class="sxs-lookup"><span data-stu-id="0e87c-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="0e87c-109">Web サービスを呼び出す</span><span class="sxs-lookup"><span data-stu-id="0e87c-109">Call web services.</span></span>
    
<span data-ttu-id="0e87c-110">UDF バイナリは、以下の 2 つの場所のいずれかにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="0e87c-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="0e87c-p102">ローカル ディレクトリ。例:</span><span class="sxs-lookup"><span data-stu-id="0e87c-p102">A local directory. For example:</span></span> 
    
    <span data-ttu-id="0e87c-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="0e87c-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="0e87c-p103">グローバル アセンブリ キャッシュ。例:</span><span class="sxs-lookup"><span data-stu-id="0e87c-p103">The global assembly cache. For example:</span></span> 
    
    <span data-ttu-id="0e87c-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="0e87c-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="0e87c-117">Office Online Server で**OfficeWebAppsExcelUserDefinedFunction**定義を作成するときに場所を参照します。</span><span class="sxs-lookup"><span data-stu-id="0e87c-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0e87c-118">Office Online Server は、ネットワーク共有にある Udf をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="0e87c-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="0e87c-119">Office Online Server で Udf を有効にする</span><span class="sxs-lookup"><span data-stu-id="0e87c-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="0e87c-120">管理者が、 [New-officewebappsfarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell コマンドレットを使用して新しい Office Web Apps サーバーファームを作成する場合、UDF アセンブリは既定で無効になっています。</span><span class="sxs-lookup"><span data-stu-id="0e87c-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="0e87c-121">**ExcelUdfsAllowed** フラグの既定値は false です。</span><span class="sxs-lookup"><span data-stu-id="0e87c-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="0e87c-122">Udf を有効にするには、office Web Apps サーバーファームが作成された後、Office Online Server で次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="0e87c-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="0e87c-123">Office Online Server で UDF 定義を作成する</span><span class="sxs-lookup"><span data-stu-id="0e87c-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="0e87c-124">UDF を有効にした後に、UDF を含むバイナリの定義を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e87c-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="0e87c-125">Office Online Server で UDF バイナリの定義を作成するには、 **OfficeWebAppsExcelUserDefinedFunction**コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="0e87c-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="0e87c-126">このコマンドレットには、次のパラメーターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e87c-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="0e87c-127">**アセンブリ**</span><span class="sxs-lookup"><span data-stu-id="0e87c-127">**Assembly**</span></span>
    
- <span data-ttu-id="0e87c-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="0e87c-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="0e87c-129">**Enable** (既定で False に設定されます)</span><span class="sxs-lookup"><span data-stu-id="0e87c-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="0e87c-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="0e87c-130">**Description**</span></span>
    
<span data-ttu-id="0e87c-131">次の例は、UDF 定義を作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0e87c-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="0e87c-132">新しい UDF 参照を作成した後、サーバーで **iisreset** を実行して、その参照をすぐに選択します。</span><span class="sxs-lookup"><span data-stu-id="0e87c-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="0e87c-133">その他の Office Online Server UDF の Windows PowerShell コマンド</span><span class="sxs-lookup"><span data-stu-id="0e87c-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="0e87c-134">Udf を操作するには、次の Windows PowerShell コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="0e87c-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="0e87c-135">**OfficeWebAppsExcelUserDefinedFunction** (必須のパラメーターはありません)-Office Online Server で構成されている UDF 定義の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="0e87c-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="0e87c-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義にプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="0e87c-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="0e87c-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義を削除します。</span><span class="sxs-lookup"><span data-stu-id="0e87c-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="0e87c-138">UDF のサンプル</span><span class="sxs-lookup"><span data-stu-id="0e87c-138">UDF sample</span></span>

<span data-ttu-id="0e87c-139">次のサンプルファイルは、UDF と UDF バイナリを使用するサンプルブックを提供しています。</span><span class="sxs-lookup"><span data-stu-id="0e87c-139">The following sample file provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="0e87c-140">[BooleanDataType](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): UDF を使用するサンプルブック</span><span class="sxs-lookup"><span data-stu-id="0e87c-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="0e87c-141">関連項目</span><span class="sxs-lookup"><span data-stu-id="0e87c-141">See also</span></span>

- [<span data-ttu-id="0e87c-142">Excel Online の管理設定を行う</span><span class="sxs-lookup"><span data-stu-id="0e87c-142">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="0e87c-143">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="0e87c-143">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-serverr)
    

