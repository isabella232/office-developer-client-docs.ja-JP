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
# <a name="configure-udfs-in-excel-online-in-office-online-server-preview"></a>Office Online Server プレビューの Excel Online での UDF の構成

[このトピックはプレリリース版のドキュメントし、将来のリリースで変更されることは]。カスタム関数を呼び出すには、Office オンライン サーバーのプレビューで Excel のオンラインでユーザー定義関数 (Udf) を使用します。 
  
Excel Online でユーザー定義関数 (UDF) を使用すると、セル内の数式を使用して、マネージ コードで記述されたカスタム関数を呼び出すことができます。UDF は、次の目的で使用できます。
  
- カスタムの数学関数を呼び出す
    
- カスタム データ ソースからデータを取得してワークシートに入力する
    
- Web サービスを呼び出す
    
UDF バイナリは、以下の 2 つの場所のいずれかにインストールできます。
  
- ローカル ディレクトリ。例: 
    
    C:\UDFs\MySampleUdf.dll
    
- グローバル アセンブリ キャッシュ。例: 
    
    CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38
    
Office オンライン サーバー プレビューの**新しい OfficeWebAppsExcelUserDefinedFunction**の定義を作成するときは、場所を参照します。 
  
> [!NOTE]
> Office オンライン サーバーのプレビューでは、ネットワーク共有上に配置する Udf をサポートしていません。 
  
## <a name="enable-udfs-on-office-online-server-preview"></a>Office オンラインのサーバーのプレビューでは、ユーザー定義関数を有効にします。

[新規 OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx)の Windows PowerShell コマンドレットを使用して、管理者が新しい Office Web アプリケーションのサーバー ファームを作成すると、UDF アセンブリは、既定で無効になります。 **ExcelUdfsAllowed**フラグの既定値は、false を指定します。 
  
Udf を有効にするには、Office Web アプリケーションのサーバー ファームを作成した後、Office オンライン サーバーのプレビューで次の Windows PowerShell コマンドを実行します。
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server-preview"></a>Office オンライン サーバーのプレビューでの UDF の定義を作成します。

Udf を有効にした後、ユーザー定義関数が含まれているバイナリの定義を作成する必要があります。 バイナリ Office オンライン サーバーのプレビューで、UDF の定義を作成するには、**新規 OfficeWebAppsExcelUserDefinedFunction**コマンドレットを使用します。 このコマンドレットには、次のパラメーターが含まれています。 
  
- **アセンブリ**
    
- **AssemblyLocation**
    
- **有効にします。**(既定では、False に設定) 
    
- **説明**
    
次の例は、UDF 定義を作成する方法を示しています。
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
新しい UDF 参照を作成した後は、すぐに参照を選択するのにはサーバー上で**iisreset**を実行します。 
  
## <a name="additional-office-online-server-preview-udf-windows-powershell-commands"></a>Office オンライン サーバー プレビュー UDF Windows PowerShell コマンドを追加

Udf を使用するには、次の Windows PowerShell コマンドレットを使用します。
  
- **Get OfficeWebAppsExcelUserDefinedFunction**(必要なパラメーターなし) の Office オンライン サーバーのプレビューに設定されている UDF の定義の一覧を返します。 
    
- **セット OfficeWebAppsExcelUserDefinedFunction**(Identity パラメーターが必要) では、既存の UDF の定義にプロパティを設定します。 
    
- **削除 OfficeWebAppsExcelUserDefinedFunction**(Identity パラメーターが必要) では、既存の UDF の定義を削除します。 
    
## <a name="udf-sample"></a>UDF のサンプル

次のファイルは、UDF と UDF バイナリを使用するサンプルのブックを提供します。
  
- [BooleanDataType.xlsx](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx) - UDF を使用するサンプル ブック  
- [EcsUdfsCommonSet.dll](http://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/EcsUdfsCommonSet.dll) - UDF バイナリ 
    
## <a name="see-also"></a>関連項目

- [Excel のオンライン管理の設定を構成します。](https://technet.microsoft.com/en-us/library/jj219698%28v=office.16%29.aspx)  
- [Office オンラインのサーバーのプレビュー](https://technet.microsoft.com/en-us/library/jj219456%28v=office.16%29.aspx)
    

