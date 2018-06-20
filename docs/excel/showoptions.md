---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798945"
---
# <a name="showoptions"></a><span data-ttu-id="24654-103">ShowOptions</span><span class="sxs-lookup"><span data-stu-id="24654-103">ShowOptions</span></span>

<span data-ttu-id="24654-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="24654-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="24654-105">ユーザーから情報を収集するモーダル ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="24654-105">Shows a modal dialog box to collect information from the user.</span></span> <span data-ttu-id="24654-106">このエントリ ポイントは、ユーザーが ([**数式**] セクションの [**詳細設定**] カテゴリ) は、[ **Excel のオプション**] ダイアログ ボックスで選択したクラスター コネクタの [**クラスターの種類**] ボックスの横の [**オプション**] ボタンをクリックしたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="24654-106">This entry point is called when a user clicks the **Options** button next to the **Cluster type** box for the selected cluster connector in the **Excel Options** dialog box (in the **Advanced** category under the **Formulas** section).</span></span> <span data-ttu-id="24654-107">クラスター コネクタは、独自のオプション] ダイアログのインターフェイスを実装して、レジストリや他の場所に関連するデータを格納するために必要があります。</span><span class="sxs-lookup"><span data-stu-id="24654-107">Cluster connectors are responsible for implementing their own options dialog interface and for storing the related data in the registry or elsewhere.</span></span> <span data-ttu-id="24654-108">オプションは、クラスター コネクタを内蔵。</span><span class="sxs-lookup"><span data-stu-id="24654-108">The options are internal to the cluster connector.</span></span> <span data-ttu-id="24654-109">Excel が認識ではありません。</span><span class="sxs-lookup"><span data-stu-id="24654-109">Excel is not aware of them.</span></span> 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a><span data-ttu-id="24654-110">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="24654-110">Parameters</span></span>

<span data-ttu-id="24654-111">_hWndParent_</span><span class="sxs-lookup"><span data-stu-id="24654-111">_hWndParent_</span></span>
  
> <span data-ttu-id="24654-112">Excel �E�C���h�E�ւ̃n���h���B</span><span class="sxs-lookup"><span data-stu-id="24654-112">A handle to the Excel window.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="24654-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="24654-113">Return value</span></span>

<span data-ttu-id="24654-114">�_�C�A���O �{�b�N�X���\�����ꂽ�ꍇ�� **xlHpcRetSuccess**�A�\������Ȃ������ꍇ�� **xlHpcRetCallFailed**�B</span><span class="sxs-lookup"><span data-stu-id="24654-114">**xlHpcRetSuccess** if the dialog box was shown; **xlHpcRetCallFailed** if it was not shown.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="24654-115">����</span><span class="sxs-lookup"><span data-stu-id="24654-115">Remarks</span></span>

<span data-ttu-id="24654-116">�N���X�^�[ �R�l�N�^�ł́A�g�p����N���X�^�[ �T�[�o�[�Ȃǂ̏�����[�U�[����擾���邽�߂ɁA���̃_�C�A���O �{�b�N�X��g�p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="24654-116">Cluster connectors can use this dialog box to get information, such as what cluster server to use, from the user.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="24654-117">�֘A����</span><span class="sxs-lookup"><span data-stu-id="24654-117">See also</span></span>

- <span data-ttu-id="24654-118">[Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)</span><span class="sxs-lookup"><span data-stu-id="24654-118">[Excel Cluster Connector Functions](excel-cluster-connector-functions.md)</span></span>

