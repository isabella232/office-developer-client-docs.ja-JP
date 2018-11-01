---
title: ビジネス オブジェクトに対してスクリプト作成の安全性を明示する
TOCTitle: Marking Business Objects as Safe for Scripting
ms:assetid: 8ee49aec-672d-96f7-baa6-9261317a4d90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249630(v=office.15)
ms:contentKeyID: 48546295
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 195e9fc25e3aa8871233ebe60441d29909b31a48
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878312"
---
# <a name="marking-business-objects-as-safe-for-scripting"></a><span data-ttu-id="08620-102">ビジネス オブジェクトに対してスクリプト作成の安全性を明示する</span><span class="sxs-lookup"><span data-stu-id="08620-102">Marking Business Objects as Safe for Scripting</span></span>


<span data-ttu-id="08620-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="08620-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="08620-p101">インターネット環境のセキュリティを確保するには、[RDS.DataSpace](dataspace-object-rds.md) オブジェクトの [CreateObject メソッド (RDS)](createobject-method-rds.md) を使用してインスタンス作成されたすべてのビジネス オブジェクトを、"スクリプトを実行しても安全" だとマークする必要があります。ビジネス オブジェクトを DCOM で使用する前に、システム レジストリの License エリアでそのようにマークされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08620-p101">To help ensure a secure Internet environment, you need to mark any business objects instantiated with the [RDS.DataSpace](dataspace-object-rds.md) object's [CreateObject](createobject-method-rds.md) method as "safe for scripting." You need to ensure they are marked as such in the License area of the system registry before they can be used in DCOM.</span></span>

<span data-ttu-id="08620-p102">ビジネス オブジェクトを、スクリプトを実行しても安全だと手動でマークするには、次のテキストを含む、拡張子 .reg のテキスト ファイルを作成します。次の 2 つの数値によって、スクリプトを実行しても安全な機能が有効になります。</span><span class="sxs-lookup"><span data-stu-id="08620-p102">To manually mark your business object as safe for scripting, create a text file with a .reg extension that contains the following text. The following two numbers enable the safe-for-scripting feature:</span></span>

```vb 
 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95801-9882-11CF-9FA9-00AA006C42C4}] 
[HKEY_CLASSES_ROOT\CLSID\<MyActiveXGUID>\Implemented 
Categories\{7DD95802-9882-11CF-9FA9-00AA006C42C4}] 
```

<span data-ttu-id="08620-108">場所\< *MyActiveXGUID* \>は、ビジネス オブジェクトの GUID の 16 進数です。</span><span class="sxs-lookup"><span data-stu-id="08620-108">where \<*MyActiveXGUID*\> is the hexadecimal GUID number of your business object.</span></span> <span data-ttu-id="08620-109">保存し、レジストリ エディターを使用するか、Windows エクスプ ローラーで .reg ファイルをダブルクリックすると、レジストリにマージすること。</span><span class="sxs-lookup"><span data-stu-id="08620-109">Save it and merge it into your registry by using the Registry Editor or double-clicking the .reg file in Windows Explorer.</span></span>

<span data-ttu-id="08620-110">Microsoft® Visual Basic 内に作成されるビジネス オブジェクトは、「スクリプトを実行しても安全」とで自動的にパッケージと展開ウィザードとマークできます。</span><span class="sxs-lookup"><span data-stu-id="08620-110">Business objects created in Microsoft® Visual Basic can be automatically marked as "safe for scripting" with the Package and Deployment Wizard.</span></span> <span data-ttu-id="08620-111">ファミリー セーフティの設定を指定するウィザードが表示されたら、ときに、**初期化**と**スクリプティングの安全性**を選択します。</span><span class="sxs-lookup"><span data-stu-id="08620-111">When the wizard asks you to specify safety settings, select **Safe for initialization** and **Safe for scripting**.</span></span>

<span data-ttu-id="08620-p105">アプリケーション セットアップ ウィザードの最後の手順では, .htm ファイルと .cab ファイルが作成されます。これらの 2 つのファイルを目的のコンピューターにコピーし, .htm ファイルをダブルクリックすると、ページを読み込んでサーバーを正しく登録できます。</span><span class="sxs-lookup"><span data-stu-id="08620-p105">On the last step, the Application Setup Wizard creates an .htm and a .cab file. You can then copy these two files to the target computer and double-click the .htm file to load the page and correctly register the server.</span></span>

<span data-ttu-id="08620-114">ビジネス オブジェクトは、Windows にインストールするため\\System32\\既定では、ディレクトリを作成は、Windows に移動\\System32 ディレクトリを変更して、 **HKEY\_クラス\_ルート\\CLSID\\ **\< *MyActiveXGUID*\>\\**InprocServer32**のレジストリ キーに正しいパスと一致します。</span><span class="sxs-lookup"><span data-stu-id="08620-114">Because the business object will be installed in the Windows\\System32\\Occache directory by default, move it to the Windows\\System32 directory and change the **HKEY\_CLASSES\_ROOT\\CLSID\\**\<*MyActiveXGUID*\>\\**InprocServer32** registry key to match the correct path.</span></span>


> [!NOTE]
> <span data-ttu-id="08620-p106">[!メモ] 初期化の安全性保持またはスクリプト化の安全性保持としてマークされたビジネス オブジェクトに対しては、ネットワーク上のどのユーザーもインスタンス作成および初期化を実行できます。カスタム ビジネス オブジェクトは、不用意にデザインされたり実装されたりしないようにする必要があります。このようなオブジェクトが、ハッカーがホスト サーバーの重要な領域にアクセスして損害を及ぼすという、セキュリティ上の脅威を招かないよう注意してください。</span><span class="sxs-lookup"><span data-stu-id="08620-p106">Business objects marked as safe for scripting or safe for initialization can be instantiated and initialized by anyone over the network. Any custom business object must not be designed and implemented casually. It is imperative that such objects do not present a security threat that hackers can explore to gain access to the sensitive area of the hosting server and inflict damages.</span></span>


