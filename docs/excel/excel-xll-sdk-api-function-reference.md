---
title: Excel XLL SDK API �֐����t�@�����X
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api function reference [excel 2007],functions [Excel 2007],reference [Excel 2007],Excel 2007 XLL Software Development Kit, reference
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798874"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="43b07-104">Excel XLL SDK API �֐����t�@�����X</span><span class="sxs-lookup"><span data-stu-id="43b07-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="43b07-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="43b07-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="43b07-106">Microsoft Excel 2013 XLL SDK �ɂ́AXLL �̋L�q����������邽�߂ɐ݌v���ꂽ�t���[�����[�N ���C�u�����̃\�[�X �t�@�C���� 2 �̃T���v�� �v���W�F�N�g (Example �� Generic) ���܂܂�܂��B</span><span class="sxs-lookup"><span data-stu-id="43b07-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="43b07-107">���̃Z�N�V�����ł́A���̊֐����t�@�����X��񋟂��܂��B</span><span class="sxs-lookup"><span data-stu-id="43b07-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="43b07-108">XLL �t�@�C�����Ăяo�����Ƃ̂ł��� Excel �R�[���o�b�N�B</span><span class="sxs-lookup"><span data-stu-id="43b07-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="43b07-109">Microsoft Excel ���������� XLL �R�[���o�b�N�B</span><span class="sxs-lookup"><span data-stu-id="43b07-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="43b07-110">�T���v���ƃt���[�����[�N�̃v���W�F�N�g�̎�v�ȋ@�\�B</span><span class="sxs-lookup"><span data-stu-id="43b07-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="43b07-111">サンプル プロジェクト</span><span class="sxs-lookup"><span data-stu-id="43b07-111">Sample projects</span></span>

<span data-ttu-id="43b07-112">Excel 2013 XLL SDK �ɂ́A���̃T���v�� �v���W�F�N�g�̃\�[�X �t�@�C���� Microsoft Visual Studio �̃v���W�F�N�g �t�@�C�����܂܂�܂��B</span><span class="sxs-lookup"><span data-stu-id="43b07-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="43b07-113">**フレームワーク**プロジェクト (`SAMPLES\FRAMEWRK\`) FRAMEWRK.lib で、他の XLL プロジェクトにリンクすることができます、ライブラリにビルドできるプロジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="43b07-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="43b07-114">ライブラリには、多くの関数や Xll に簡単に記述するためのツールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="43b07-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="43b07-115">このライブラリは、ヘッダー ファイル FRAMEWRK.h を使用して、連携して、他のプロジェクトの両方で使用されます。</span><span class="sxs-lookup"><span data-stu-id="43b07-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="43b07-116">**例**プロジェクト (`SAMPLES\EXAMPLE\`)、xll ファイルの EXAMPLE.xll をビルドできるプロジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="43b07-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="43b07-117">Xll ファイルには、フレームワーク ライブラリを使用し、XLL アドイン インターフェイスなどの機能の**xlAutoOpen**の実装の例の多くの例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="43b07-117">The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="43b07-118">**汎用的な**プロジェクト (`SAMPLES\GENERIC\`)、xll ファイルの GENERIC.xll をビルドできるプロジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="43b07-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="43b07-119">Xll ファイルはいくつかの例の関数とコマンドの例を示します、独自の Xll を記述するための開始点です。</span><span class="sxs-lookup"><span data-stu-id="43b07-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="43b07-120">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="43b07-120">In this section</span></span>

- <span data-ttu-id="43b07-121">[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)</span><span class="sxs-lookup"><span data-stu-id="43b07-121">[Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)</span></span>
  
- <span data-ttu-id="43b07-122">[C API �R�[���o�b�N�֐� Excel4�AExcel12](c-api-callback-functions-excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="43b07-122">[C API Callback Functions Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)</span></span>
  
- [<span data-ttu-id="43b07-123">�d�v�Ŗ�ɗ��� C API XLM �֐�</span><span class="sxs-lookup"><span data-stu-id="43b07-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="43b07-124">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="43b07-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- <span data-ttu-id="43b07-125">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="43b07-125">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>
  
- [<span data-ttu-id="43b07-126">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="43b07-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- <span data-ttu-id="43b07-127">[Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)</span><span class="sxs-lookup"><span data-stu-id="43b07-127">[Excel Cluster Connector Functions](excel-cluster-connector-functions.md)</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43b07-128">�֘A����</span><span class="sxs-lookup"><span data-stu-id="43b07-128">See also</span></span>

- [<span data-ttu-id="43b07-129">Excel �ł� C API ��g�p�����v���O���~���O</span><span class="sxs-lookup"><span data-stu-id="43b07-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="43b07-130">Excel XLL �̊J��</span><span class="sxs-lookup"><span data-stu-id="43b07-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

