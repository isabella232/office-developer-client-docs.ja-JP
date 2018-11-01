---
title: RunSavedImportExport マクロ アクション
TOCTitle: RunSavedImportExport Macro Action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 48e808fa27e468dd7cb651cb5784627d5064fea0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870934"
---
# <a name="runsavedimportexport-macro-action"></a><span data-ttu-id="916c0-102">RunSavedImportExport マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="916c0-102">RunSavedImportExport Macro Action</span></span>


<span data-ttu-id="916c0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="916c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="916c0-104">**RunSavedImportExport** アクションを使用すると、インポート ウィザードまたはエクスポート ウィザードを使用して作成した保存済みのインポート定義またはエクスポート定義を実行できます。</span><span class="sxs-lookup"><span data-stu-id="916c0-104">You can use the **RunSavedImportExport** action to run a saved import or export specification that you created by using the Import Wizard or the Export Wizard.</span></span>


> [!NOTE]
> <P><span data-ttu-id="916c0-p101">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="916c0-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="916c0-107">設定</span><span class="sxs-lookup"><span data-stu-id="916c0-107">Setting</span></span>

<span data-ttu-id="916c0-108">**RunSavedImportExport** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="916c0-108">The **RunSavedImportExport** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="916c0-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="916c0-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="916c0-110">説明</span><span class="sxs-lookup"><span data-stu-id="916c0-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="916c0-111"><strong>Saved Import Export Name/保存済みのインポート/エクスポート操作の名前</strong></span><span class="sxs-lookup"><span data-stu-id="916c0-111"><strong>Saved Import Export Name</strong></span></span></p></td>
<td><p><span data-ttu-id="916c0-112">ドロップダウン リストから、保存済みのインポート定義またはエクスポート定義の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="916c0-112">Select the name of a saved import or export specification from the drop-down list.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="916c0-113">解説</span><span class="sxs-lookup"><span data-stu-id="916c0-113">Remarks</span></span>

  - <span data-ttu-id="916c0-114">このマクロ アクションの動作は、Access で次の操作を実行した場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="916c0-114">This macro action has the same effect as performing the following procedure in Access:</span></span>
    
    1.  <span data-ttu-id="916c0-115">[ **外部データ**] タブで、[ **保存済みのインポート操作**] または [ **保存済みのエクスポート操作**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="916c0-115">On the **External Data** tab, click either **Saved Imports** or **Saved Exports**.</span></span>
    
    2.  <span data-ttu-id="916c0-116">[ **データ タスクの管理**] ダイアログ ボックスの [ **保存済みのインポート操作**] タブまたは [ **保存済みのエクスポート操作**] タブ (前の手順で選択した操作によります) で、実行する定義をクリックします。</span><span class="sxs-lookup"><span data-stu-id="916c0-116">In the **Manage Data Tasks** dialog box, on the **Saved Imports** or **Saved Exports** tab (depending on your choice in the preceding step), click the specification that you want to run.</span></span>
    
    3.  <span data-ttu-id="916c0-117">[ **実行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="916c0-117">Click **Run**.</span></span>

  - <span data-ttu-id="916c0-118">**RunSavedImportExport** アクションを実行する前に、インポート元ファイルとエクスポート先ファイルが存在し、インポート元データのインポートの準備ができていることを確認して、この操作によってエクスポート先ファイルのデータが誤って上書きされないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="916c0-118">Before running the **RunSavedImportExport** action, make sure that the source and destination files exist, the source data is ready for importing, and that the operation will not accidentally overwrite any data in your destination file.</span></span>

  - <span data-ttu-id="916c0-119">インポート定義およびエクスポート定義の保存と実行の詳細については、「 **参照**」セクションのリンク先を参照してください。</span><span class="sxs-lookup"><span data-stu-id="916c0-119">Find links to more information about saving and running import and export specifications in the **See Also** section.</span></span>

  - <span data-ttu-id="916c0-120">保存されているインポートまたはエクスポート定義のマクロを作成した後で**インポート エクスポート名を保存された**引数が削除された場合に選択するが表示されます、次のエラー メッセージ、マクロの実行時:**で指定したインデックスの仕様は存在しません。別のインデックスを指定します。'仕様の名前。' です。** 。</span><span class="sxs-lookup"><span data-stu-id="916c0-120">If the saved import or export specification you choose for the **Saved Import Export Name** argument is deleted after the macro is created, Access displays the following error message when the macro is run: **The specification with the specified index does not exist. Specify a different index. '\*\*\*\*\*specification name\*\*\*\*\*'.**</span></span>

