---
title: Office オンライン サーバーでオンラインに Excel でユーザー定義関数を構成します。
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Office オンライン サーバーで Excel のオンラインでカスタム関数を呼び出すユーザー定義関数 (Udf) を使用します。
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722789"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="a1c03-103">Office オンライン サーバーでオンラインに Excel でユーザー定義関数を構成します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="a1c03-104">Office オンライン サーバーで Excel のオンラインでカスタム関数を呼び出すユーザー定義関数 (Udf) を使用します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="a1c03-p101">Excel Online でユーザー定義関数 (UDF) を使用すると、セル内の数式を使用して、マネージ コードで記述されたカスタム関数を呼び出すことができます。UDF は、次の目的で使用できます。</span><span class="sxs-lookup"><span data-stu-id="a1c03-p101">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells. You can use UDFs to:</span></span>
  
- <span data-ttu-id="a1c03-107">カスタムの数学関数を呼び出す</span><span class="sxs-lookup"><span data-stu-id="a1c03-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="a1c03-108">カスタム データ ソースからデータを取得してワークシートに入力する</span><span class="sxs-lookup"><span data-stu-id="a1c03-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="a1c03-109">Web サービスを呼び出す</span><span class="sxs-lookup"><span data-stu-id="a1c03-109">Call web services.</span></span>
    
<span data-ttu-id="a1c03-110">UDF バイナリは、以下の 2 つの場所のいずれかにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="a1c03-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="a1c03-p102">ローカル ディレクトリ。例:</span><span class="sxs-lookup"><span data-stu-id="a1c03-p102">A local directory. For example:</span></span> 
    
    <span data-ttu-id="a1c03-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="a1c03-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="a1c03-p103">グローバル アセンブリ キャッシュ。例:</span><span class="sxs-lookup"><span data-stu-id="a1c03-p103">The global assembly cache. For example:</span></span> 
    
    <span data-ttu-id="a1c03-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="a1c03-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="a1c03-117">Office オンライン サーバーで**新しい OfficeWebAppsExcelUserDefinedFunction**の定義を作成するときは、場所を参照します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a1c03-118">Office オンラインのサーバーは、ネットワーク共有上に配置する Udf をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="a1c03-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="a1c03-119">Office オンラインのサーバー上のユーザー定義関数を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a1c03-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="a1c03-120">[新規 OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx)の Windows PowerShell コマンドレットを使用して、管理者が新しい Office Web アプリケーションのサーバー ファームを作成すると、UDF アセンブリは、既定で無効になります。</span><span class="sxs-lookup"><span data-stu-id="a1c03-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="a1c03-121">**ExcelUdfsAllowed**フラグの既定値は、false を指定します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="a1c03-122">Udf を有効にするには、Office Web アプリケーションのサーバー ファームを作成した後、Office オンライン サーバーで、次の Windows PowerShell コマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="a1c03-123">Office オンラインのサーバー上の UDF の定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="a1c03-124">Udf を有効にした後、ユーザー定義関数が含まれているバイナリの定義を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1c03-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="a1c03-125">Office オンライン サーバーでバイナリ、UDF の定義を作成するには、**新規 OfficeWebAppsExcelUserDefinedFunction**コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="a1c03-126">このコマンドレットには、次のパラメーターが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a1c03-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="a1c03-127">**アセンブリ**</span><span class="sxs-lookup"><span data-stu-id="a1c03-127">**Assembly**</span></span>
    
- <span data-ttu-id="a1c03-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="a1c03-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="a1c03-129">**Enable** (既定で False に設定されます)</span><span class="sxs-lookup"><span data-stu-id="a1c03-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="a1c03-130">**説明**</span><span class="sxs-lookup"><span data-stu-id="a1c03-130">**Description**</span></span>
    
<span data-ttu-id="a1c03-131">次の例は、UDF 定義を作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a1c03-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="a1c03-132">新しい UDF 参照を作成した後、サーバーで **iisreset** を実行して、その参照をすぐに選択します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="a1c03-133">Office オンライン サーバー UDF の Windows PowerShell コマンドを追加</span><span class="sxs-lookup"><span data-stu-id="a1c03-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="a1c03-134">Udf を使用するには、次の Windows PowerShell コマンドレットを使用します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="a1c03-135">**Get OfficeWebAppsExcelUserDefinedFunction**(必要なパラメーターなし) の Office オンライン サーバーで構成されている UDF の定義の一覧を返します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="a1c03-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義にプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="a1c03-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (ID パラメーターが必要) - 既存の UDF 定義を削除します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="a1c03-138">UDF のサンプル</span><span class="sxs-lookup"><span data-stu-id="a1c03-138">UDF sample</span></span>

<span data-ttu-id="a1c03-139">次のファイルは、UDF と UDF バイナリを使用するサンプルのブックを提供します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-139">The following files provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="a1c03-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): UDF を使用するサンプル ブック</span><span class="sxs-lookup"><span data-stu-id="a1c03-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
- <span data-ttu-id="a1c03-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): UDF バイナリ</span><span class="sxs-lookup"><span data-stu-id="a1c03-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): the UDF binary</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a1c03-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1c03-142">See also</span></span>

- [<span data-ttu-id="a1c03-143">Excel のオンライン管理の設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="a1c03-143">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="a1c03-144">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="a1c03-144">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

