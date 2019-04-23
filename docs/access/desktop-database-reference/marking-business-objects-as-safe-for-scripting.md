---
title: スクリプト実行に安全なビジネス オブジェクトとしてマークする
TOCTitle: Marking business objects as safe for scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe5d331b7f3ab4685cb930323076d111a25ec68e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289778"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a><span data-ttu-id="a1941-102">スクリプト実行に安全なビジネス オブジェクトとしてマークする</span><span class="sxs-lookup"><span data-stu-id="a1941-102">Marking business objects as safe for scripting</span></span>

<span data-ttu-id="a1941-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1941-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1941-p101">インターネット環境のセキュリティを確保するには、[RDS.DataSpace](dataspace-object-rds.md) オブジェクトの [CreateObject メソッド (RDS)](createobject-method-rds.md) を使用してインスタンス作成されたすべてのビジネス オブジェクトを、"スクリプトを実行しても安全" だとマークする必要があります。ビジネス オブジェクトを DCOM で使用する前に、システム レジストリの License エリアでそのようにマークされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1941-p101">To help ensure a secure Internet environment, you need to mark any business objects instantiated with the [RDS.DataSpace](dataspace-object-rds.md) object's [CreateObject](createobject-method-rds.md) method as "safe for scripting." You need to ensure they are marked as such in the License area of the system registry before they can be used in DCOM.</span></span>

<span data-ttu-id="a1941-p102">ビジネス オブジェクトを、スクリプトを実行しても安全だと手動でマークするには、次のテキストを含む、拡張子 .reg のテキスト ファイルを作成します。次の 2 つの数値によって、スクリプトを実行しても安全な機能が有効になります。</span><span class="sxs-lookup"><span data-stu-id="a1941-p102">To manually mark your business object as safe for scripting, create a text file with a .reg extension that contains the following text. The following two numbers enable the safe-for-scripting feature:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

<span data-ttu-id="a1941-108">\< *myactivexguid* \>は、ビジネスオブジェクトの16進数の guid 番号です。</span><span class="sxs-lookup"><span data-stu-id="a1941-108">where \<*MyActiveXGUID*\> is the hexadecimal GUID number of your business object.</span></span> <span data-ttu-id="a1941-109">Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="a1941-109">Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</span></span>

<span data-ttu-id="a1941-110">Microsoft Visual Basic で作成されたビジネスオブジェクトは、パッケージと展開ウィザードを使用して、自動的に "スクリプトを実行しても安全" とマークできます。</span><span class="sxs-lookup"><span data-stu-id="a1941-110">Business objects created in Microsoft Visual Basic can be automatically marked as "safe for scripting" with the Package and Deployment Wizard.</span></span> <span data-ttu-id="a1941-111">When the wizard asks you to specify safety settings, select **Safe for initialization** and **Safe for scripting**.</span><span class="sxs-lookup"><span data-stu-id="a1941-111">When the wizard asks you to specify safety settings, select **Safe for initialization** and **Safe for scripting**.</span></span>

<span data-ttu-id="a1941-p105">アプリケーション セットアップ ウィザードの最後の手順では, .htm ファイルと .cab ファイルが作成されます。これらの 2 つのファイルを目的のコンピューターにコピーし, .htm ファイルをダブルクリックすると、ページを読み込んでサーバーを正しく登録できます。</span><span class="sxs-lookup"><span data-stu-id="a1941-p105">On the last step, the Application Setup Wizard creates an .htm and a .cab file. You can then copy these two files to the target computer and double-click the .htm file to load the page and correctly register the server.</span></span>

<span data-ttu-id="a1941-114">ビジネスオブジェクトは\\既定で windows system32\\occache ディレクトリにインストールされるため、windows\\system32 ディレクトリに移動し、 **HKEY\_クラス\_のルート\\CLSID\\ **を変更します。\< *myactivexguid*\>\\**InprocServer32**レジストリキーを正しいパスに一致させます。</span><span class="sxs-lookup"><span data-stu-id="a1941-114">Because the business object will be installed in the Windows\\System32\\Occache directory by default, move it to the Windows\\System32 directory and change the **HKEY\_CLASSES\_ROOT\\CLSID\\**\<*MyActiveXGUID*\>\\**InprocServer32** registry key to match the correct path.</span></span>


> [!NOTE]
> <span data-ttu-id="a1941-p106">[!メモ] 初期化の安全性保持またはスクリプト化の安全性保持としてマークされたビジネス オブジェクトに対しては、ネットワーク上のどのユーザーもインスタンス作成および初期化を実行できます。カスタム ビジネス オブジェクトは、不用意にデザインされたり実装されたりしないようにする必要があります。このようなオブジェクトが、ハッカーがホスト サーバーの重要な領域にアクセスして損害を及ぼすという、セキュリティ上の脅威を招かないよう注意してください。</span><span class="sxs-lookup"><span data-stu-id="a1941-p106">Business objects marked as safe for scripting or safe for initialization can be instantiated and initialized by anyone over the network. Any custom business object must not be designed and implemented casually. It is imperative that such objects do not present a security threat that hackers can explore to gain access to the sensitive area of the hosting server and inflict damages.</span></span>


