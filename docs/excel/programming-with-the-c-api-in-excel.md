---
title: Excel �ł� C API ��g�p�����v���O���~���O
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007],programming interfaces [Excel 2007],C API [Excel 2007], when to use,C API [Excel 2007], relation to XLM,Excel programming interfaces
localization_priority: Normal
ms.assetid: 142bc0ce-7d16-4b69-9799-ce6558da2def
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 459e57d41ef7497c535e51944bbaf24daee84167
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798939"
---
# <a name="programming-with-the-c-api-in-excel"></a><span data-ttu-id="0ab1b-104">Excel �ł� C API ��g�p�����v���O���~���O</span><span class="sxs-lookup"><span data-stu-id="0ab1b-104">Programming with the C API in Excel</span></span>

 <span data-ttu-id="0ab1b-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0ab1b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0ab1b-p101">Microsoft Excel 2013 XLL �\�t�g�E�F�A�J���L�b�g�� C API ��g�p���āAExcel 2013 �̍��p�t�H�[�}���X�̃��[�N�V�[�g�֐���쐬�ł��܂��BExcel 2013 �� C API �ւ̃A�b�v�O���[�h�́A�T�[�h �p�[�e�B���@�\�܂��͓���@�\�̃p�t�H�[�}���X���d�v�ȈӖ�������[�U�[�ɑ΂��Čp�����čs���Ă���T�|�[�g�𔽉f���܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p101">You can use the Microsoft Excel 2013 XLL Software Development Kit and the C API to create high-performance worksheet functions for Excel 2013. The upgrades to the Excel 2013 C API reflect ongoing support for users for whom the performance of third-party or in-house functionality is critical.</span></span>
  
## <a name="excel-programming-interfaces"></a><span data-ttu-id="0ab1b-108">Excel �̃v���O���~���O �C���^�[�t�F�C�X</span><span class="sxs-lookup"><span data-stu-id="0ab1b-108">Excel Programming Interfaces</span></span>

<span data-ttu-id="0ab1b-p102">Excel �ɂ́A�C���^�[�t�F�C�X��g�p���� Excel �Ɛڑ�����A�v���P�[�V������J�����邽�߂̂������̃I�v�V�������p�ӂ���Ă��܂��BExcel �̃v���O���~���O �C���^�[�t�F�C�X�́A���̏����ňȑO�̃o�[�W�����ɒǉ�����܂����B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p102">Excel provides several options for developing applications that interface with it. The Excel programming interfaces were added to earlier versions in the following order:</span></span>
  
- <span data-ttu-id="0ab1b-p103">**XLM �}�N������:** Excel �̊g���@�\�̂��߂Ƀ��[�U�[���g�p�ł���ŏ��̌���ŁAC API �̊�b�ɂȂ�܂����BXLM �́AExcel 2010 �ł�T�|�[�g����Ă��܂������A���Ȃ�ȑO�� Visual Basic for Applications (VBA) �ɒu���������܂����B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p103">**XLM macro language:** The first user-accessible language for the extension of Excel and the basis of the C API. Although still supported in Excel 2010, XLM has long been superseded by Visual Basic for Applications (VBA).</span></span> 
    
- <span data-ttu-id="0ab1b-p104">**C API �� XLL:** Excel �ɓ�������Ă��� DLL �ł��B������ DLL �́A���p�t�H�[�}���X�̃��[�N�V�[�g�֐���ǉ�����ł���ړI�ōő��̃C���^�[�t�F�C�X��񋟂��܂��B�������A����ȍ~�̋Z�p�Ɣ�r���Ă����炩���G�ł��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p104">**C API and XLLs:** DLLs that are integrated with Excel. These DLLs provide the most direct and fastest interface for the addition of high-performance worksheet functions, although at the cost of some complexity compared with later technologies.</span></span> 
    
- <span data-ttu-id="0ab1b-p105">**VBA:** Excel �u�b�N �I�u�W�F�N�g�Ɋ֘A�t�����Ă��� Visual Basic �R�[�h �I�u�W�F�N�g�ł��BVBA �́A�C�x���g �g���b�v�A�J�X�^�}�C�Y�A���[�U�[��\`�֐��ƃR�}���h�̒ǉ���\�ɂ��Ă��܂��BVBA �́A�ł��ʓI�Ɏg�p����A�ł�e�Ղɗ��p�ł���g���I�v�V�����ł��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p105">**VBA:** Visual Basic code objects that are associated with Excel workbook objects. VBA allows event trapping, customization, and the addition of user-defined functions and commands. VBA is the most commonly used and most easily available of the extensibility options.</span></span> 
    
- <span data-ttu-id="0ab1b-p106">**COM:** Windows �x�[�X�̃A�v���P�[�V���������̑��݉^�p���̕W���ł��BExcel �́A������ăC�x���g��I�u�W�F�N�g����J���܂��BVBA �́ACOM ��g�p���� Excel �ƑΘb���܂��BExcel �́A�O������ Excel �𐧌䂷�� C++ COM �R�[�h�̃��\�[�X��A�v���P�[�V������쐬����̂ɖ𗧂� COM �^�C�v ���C�u������G�N�X�|�[�g���܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p106">**COM:** The interoperability standard for Windows-based applications, through which Excel exposes its events and objects. VBA uses COM to interact with Excel. Excel exports COM type libraries that can help you create C++ COM code resources and applications that can control Excel externally.</span></span> 
    
- <span data-ttu-id="0ab1b-p107">**Microsoft .NET Framework:** ���U���̐v���ȃA�v���P�[�V�����J���p�ɐ݌v���ꂽ�A��������}�l�[�W �R�[�h���ł��B.NET Framework �����̃R�[�h�̎�v�ȃv���O���~���O����� C# �ł����A�����̌���� Microsoft ���Ԍ��� (MSIL) �ɃR���p�C���ł��܂��BExcel 2013 �ł�, .NET Framework �A�Z���u���Ɋ܂܂��R�[�h ���\�[�X�ɃA�N�Z�X�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p107">**The Microsoft .NET Framework:** The multi-language managed code environment designed for rapid application development for distributed environments. The primary programming language for code that is based on the .NET Framework is C#, although many languages can be compiled to the Microsoft intermediate language (MSIL). Excel 2013 can access code resources contained within .NET Framework assemblies.</span></span> 
    
## <a name="when-to-use-the-c-api"></a><span data-ttu-id="0ab1b-124">C API ��g�p����ꍇ</span><span class="sxs-lookup"><span data-stu-id="0ab1b-124">When to Use the C API</span></span>

<span data-ttu-id="0ab1b-125">Xll を記述し、C API を使用する主な理由としては、高性能なワークシート関数を作成します。</span><span class="sxs-lookup"><span data-stu-id="0ab1b-125">The primary reason for writing XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="0ab1b-126">XLL 関数は、ユーザー定義関数、Xll にする技術のほとんどのユーザーは現実的ではありませんを記述するために必要なスキルと知識を取得する時間の投資とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="0ab1b-126">Although XLL functions are frequently referred to as user-defined functions, the investment in time to obtain the understanding and skills that are required to write XLLs make this a technology impractical for most users.</span></span> <span data-ttu-id="0ab1b-127">関数の高パフォーマンスのアプリケーションではそれにもかかわらず、- と Excel 2013、強力なサーバー リソースをマルチ スレッドのインターフェイスを記述する機能、これを Excel の機能拡張の非常に重要な一部にします。</span><span class="sxs-lookup"><span data-stu-id="0ab1b-127">Nevertheless, the applications of high-performance functions—and, in Excel 2013, the ability to write multithreaded interfaces to powerful server resources—make this a very important part of Excel extensibility.</span></span> 
  
<span data-ttu-id="0ab1b-128">Excel 2007 �œ������ꂽ C API �̉����́A���[�U�[ �C���^�[�t�F�C�X�Ȃǂ̋@�\�ł͂Ȃ��A��ɍ����\�Ȍv�Z�Ɋ֘A���鑤�ʂɊ֌W���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-128">The revision of the C API that was introduced in Excel 2007 is mainly concerned with the aspects relating to high-performance calculations, rather than features such as the user interface.</span></span>
  
### <a name="writing-high-performance-user-defined-worksheet-functions"></a><span data-ttu-id="0ab1b-129">���p�t�H�[�}���X�̃��[�U�[��\`���[�N�V�[�g�֐��̍쐬</span><span class="sxs-lookup"><span data-stu-id="0ab1b-129">Writing High-Performance User-Defined Worksheet Functions</span></span>

<span data-ttu-id="0ab1b-p109">XLL �A�h�C����쐬���āA���p�t�H�[�}���X�̃��[�N�V�[�g�֐���쐬����ꍇ�AExcel �� C API �͗��z�I�ȑI����ł��BC API ��g�p����ƁA���[�N�V�[�g�̃f�[�^�֍ł���ړI�ɃA�N�Z�X�ł��܂��BXLL ��g�p����ƁAExcel �� DLL ���\�[�X�֍ł���ړI�ɃA�N�Z�X�ł���悤�ɂȂ�܂��BExcel 2013 �ł́A�V�����f�[�^�^���ǉ�����邱�Ƃɂ���āA�܂��ł�d�v�Ȃ��ƂƂ��āA�N���X�^�[�����ꂽ�T�[�o�[�ł̃��[�U�[��\`�֐��̎��s���T�|�[�g����邱�Ƃɂ���āAXLL �̃p�t�H�[�}���X�͂���Ɍ��サ�Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p109">The Excel C API is the ideal choice when you want to create high-performance worksheet functions by creating XLL add-ins. The C API provides you with the most direct access to worksheet data. XLLs provide Excel with the most direct access to the DLL resources. The performance of XLLs is further enhanced in Excel 2013 by the addition of new data types and, most importantly, support for running user-defined functions on clustered servers.</span></span>
  
<span data-ttu-id="0ab1b-p110">XLL �̎g�p�ɂ̓R�X�g��������܂��BC API �ɂ́AVBA�ACOM, .NET Framework �ɂ���A���Ȃ荂���x���̐v���ȊJ���@�\�͂���܂���B�������Ǘ��͒჌�x���ōs����̂ŁA�J���҂ɂ��傫�ȐӔC�𕉂킹�邱�ƂɂȂ�܂��BCOM �o�R�Ō��J����Ă��鑽���� Excel �@�\�́AVBA ��.NET Framework ���ė��p�ł��܂����AC API �ɂ͌��J����Ă��܂���B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p110">Working with XLLs comes at a cost: The C API has none of the higher-level rapid development features of VBA, COM, or the .NET Framework. Memory management is low level and, therefore, puts greater responsibility on the developer. Many Excel features that are exposed via COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>
  
### <a name="accessing-multithreaded-servers-by-using-xll-worksheet-functions"></a><span data-ttu-id="0ab1b-136">XLL ���[�N�V�[�g�֐���g�p�����}���\`�X���b�h �T�[�o�[�ւ̃A�N�Z�X</span><span class="sxs-lookup"><span data-stu-id="0ab1b-136">Accessing Multithreaded Servers by Using XLL Worksheet Functions</span></span>

<span data-ttu-id="0ab1b-p111">Excel 2007 で導入された、マルチ スレッド再計算 (MTR) を使用すると、スレッド セーフな XLL ワークシート関数を作成できます。マルチ スレッド サーバーにアクセスするのに、これらの関数を使用できます。以下のセクションでは、ユーザーが観察するパフォーマンスをどのように大幅に向上させることができるかを詳細に説明します。処理能力を大量に消費する必要がある Excel ユーザーに対して、MTR を使用する XLL と強力な計算サーバーの組み合わせは、最高のパフォーマンス ソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p111">Multithreaded recalculation (MTR), which was introduced in Excel 2007, enables you to create thread-safe XLL worksheet functions. You can use these functions to access multithreaded servers. Later sections describe more fully how this can dramatically increase the performance observed by the user. For Excel users who sometimes need access to a lot of processing power, the combination of an XLL that uses MTR and a powerful calculation server provides the highest-performance solution.</span></span>
  
### <a name="customizing-the-excel-user-interface"></a><span data-ttu-id="0ab1b-141">Excel ���[�U�[ �C���^�[�t�F�C�X�̃J�X�^�}�C�Y</span><span class="sxs-lookup"><span data-stu-id="0ab1b-141">Customizing the Excel User Interface</span></span>

<span data-ttu-id="0ab1b-p112">Excel �̑����̃o�[�W�����ł́AC API �̓��[�U�[ �C���^�[�t�F�C�X��J�X�^�}�C�Y����ۂɁA�œK�ȑI����ł͂���܂���ł����BVBA �́AExcel �̃I�u�W�F�N�g�ƃC�x���g�ւ̃A�N�Z�X�ɗD��Ă��܂��BExcel 2007 �œ������ꂽ���[�U�[ �C���^�[�t�F�C�X�́A�O�ςƊ�{�Z�p�̗��ʂŁA�ȑO�̃o�[�W�����Ƃ͑傫���قȂ�܂��B�}�l�[�W �R�[�h�̃��\�[�X��g�p���āA���̃C���^�[�t�F�C�X��œK�ɃJ�X�^�}�C�Y�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p112">For many versions of Excel, the C API has not been the best choice for customizing the user interface. VBA has superior access to Excel objects and events. The user interface introduced in Excel 2007 is significantly different from earlier versions both in appearance and underlying technology. You can best customize this interface by using managed code resources.</span></span>
  
### <a name="creating-applications-that-can-be-accessed-on-the-internet"></a><span data-ttu-id="0ab1b-146">�C���^�[�l�b�g��ŃA�N�Z�X�\�ȃA�v���P�[�V�����̍쐬</span><span class="sxs-lookup"><span data-stu-id="0ab1b-146">Creating Applications that Can Be Accessed on the Internet</span></span>

<span data-ttu-id="0ab1b-p113">2007 Microsoft Office system �œ������ꂽ Excel Services �ł́A�W���� Web �u���E�U�[ �c�[����g�p���āA���[�U�[���u�b�N�� Excel �̋@�\�ɃA�N�Z�X����őP�̕��@��񋟂��܂��B.NET Framework �J������ƃ��\�[�X�Ƌ��ɁA�����̋Z�p�͏����ɓn���ă��[�U�[�ɂƂ��� Excel �W�J�̏d�v�ȕ����ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p113">Excel Services, introduced with the 2007 Microsoft Office system, provides the best way to give users access to workbooks and Excel functionality by using standard Web browser tools. Together with .NET Framework development languages and resources, these technologies represent an important part of Excel deployment to users in the future.</span></span>
  
### <a name="controlling-excel-from-external-applications"></a><span data-ttu-id="0ab1b-149">�O���A�v���P�[�V��������� Excel �̐���</span><span class="sxs-lookup"><span data-stu-id="0ab1b-149">Controlling Excel from External Applications</span></span>

<span data-ttu-id="0ab1b-p114">Excel �́A���̃I�u�W�F�N�g�A���\�b�h�A�C�x���g�� COM �C���^�[�t�F�C�X�o�R�Ō��J���܂��B���������āAExcel �Z�b�V������J�n���Đ��䂵����A������ Excel �Z�b�V�����𐧌䂵���肷��X�^���h�A���� �A�v���P�[�V������쐬���邽�߂� COM ��g�p�ł��܂��BC++ �� VBA ��܂ށA�������̊J������� COM �Ɍ��J����Ă��� Excel �C���^�[�t�F�C�X�ɃA�N�Z�X�ł��܂��BC# �� .NET Framework �ł́A���l�� Excel �ւ̃����[�g �A�N�Z�X�Ɛ����\�ɂ��� Excel �ւ̃C���^�[�t�F�C�X��񋟂��܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p114">Excel exposes its objects, methods, and events through the COM interface. You can, therefore, use COM to create stand-alone applications that can start and control an Excel session or control an existing Excel session. You can access the COM-exposed Excel interface within several development languages, including C++ and VBA. C# and the .NET Framework similarly provide an interface to Excel that enables remote access to and control of Excel.</span></span>
  
## <a name="asynchronous-calling-of-excel"></a><span data-ttu-id="0ab1b-154">Excel �̔񓯊��Ăяo��</span><span class="sxs-lookup"><span data-stu-id="0ab1b-154">Asynchronous Calling of Excel</span></span>

<span data-ttu-id="0ab1b-p115">Excel �� XLL �ɐ������łɓn���Ă���ꍇ�ɂ̂݁AXLL �� C API ��Ăяo�����Ƃ��ł���悤�ɂ��܂��BExcel ���Ăяo�����[�N�V�[�g�֐��́AC API ��g�p���� Excel �ɃR�[���o�b�N�ł��܂��BExcel ���Ăяo�� XLL �R�}���h�́AC API ��Ăяo�����Ƃ��ł��܂��BVBA ���ꎩ�̂� Excel �ɂ���ČĂяo�����Ƃ��� VBA ���Ăяo�� DLL�AXLL �֐��A�R�}���h�́AC API ��Ăяo�����Ƃ��ł��܂��B���Ƃ��΁A���Ԏw��� Windows �R�[���o�b�N�� XLL �ɐݒ肵�A���� XLL ���� C API ��Ăяo�����Ƃ͂ł��܂���B�܂��AXLL �ɂ���č쐬���ꂽ�o�b�N �O���E���h �X���b�h���� C API ��Ăяo�����Ƃ�ł��܂���BDLL �܂��� XLL ���� COM ��g�p���Ĕ񓯊��� Excel ��Ăяo�����Ƃ͂����߂ł��܂���B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p115">Excel allows XLLs to call the C API only when Excel has passed control to the XLL. A worksheet function that is called by Excel can call back into Excel by using the C API. An XLL command that is called by Excel can call the C API. DLL and XLL functions and commands that are called by VBA when VBA has itself been called by Excel can call the C API. You cannot, for example, set a timed Windows callback into your XLL and call the C API from it, and you cannot call the C API from a background thread created by your XLL. Calling Excel asynchronously by using COM from a DLL or XLL is not recommended.</span></span>
  
<span data-ttu-id="0ab1b-p116">�C�x���g�ɔ񓯊��ɉ������� Excel �̃A�v���P�[�V����������ꍇ�A����ɂ͑����̐���������܂��B���Ƃ��΁AExcel ���C���^�[�l�b�g��̃f�[�^�̈ꕔ��擾���A�f�[�^���ύX����邽�тɍČv�Z����悤�ɂ������Ƃ��܂��B���邢�́A�o�b�N�O���E���h �X���b�h�Ōv�Z����s���A���̏I������ Excel ���Čv�Z����悤�ɂ������ꍇ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p116">This is very limiting because there may be applications in which you want Excel to react to an event asynchronously. For example, you might want Excel to retrieve a piece of data on the Internet and recalculate whenever that data changes. Or you might want a background thread to perform a calculation and have Excel recalculate when it is finished.</span></span>
  
<span data-ttu-id="0ab1b-p117">Excel ���ύX��A�N�e�B�u�Ƀ|�[�����O����悤�ɂ���Ύ����ł��܂����A����� Excel ���p�ɂɒʏ�̏����𒆒f����̂Ō����I�ł͂���܂��񂵁A����������܂��B���z�I�ȃ\�����[�V�����ł͂���܂��񂪁AC API �܂��� VBA ��g�p���āA���Ԏw��ŌJ��Ԃ��R�}���h��ݒ肷�邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p117">You can do this by having Excel actively poll for changes, but this is inefficient and limiting because it involves Excel frequently interrupting its regular activity. You can set up repeated timed command using the C API or VBA, although this is not an ideal solution.</span></span>
  
<span data-ttu-id="0ab1b-p118">理想的には、データの変更を検出し、Excel をトリガーして更新の取得と再計算を実行させる、より効率的な外部プロセスが望まれます。COM を使用して Excel とインターフェイスを介して接続するアプリケーションを使用することによって、これを実現できます。Excel が明示的に制御を渡す場合にのみ呼び出す C API と同じような制限は COM にはありません。ダイアログボックスが表示されていたり、メニューがプルダウンされていたり、マクロが実行されている場合は、メソッドの呼び出しは無視されます。しかし、Excel が準備完了状態のときにはいつでも、COM アプリケーションは Excel メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p118">Ideally you would want a more efficient external process to check for the change in data, and for that external process to trigger Excel to retrieve the update and perform a recalculation. You can do this by using an application that interfaces to Excel by using COM. COM is not restricted in the same manner as the C API to making calls only when Excel has explicitly passed it control. COM applications can invoke Excel methods whenever Excel is in a ready state, although these method calls might be ignored if dialog boxes are being displayed, menus are pulled down, or when a macro is executing.</span></span>
  
## <a name="c-api-and-its-relation-to-xlm"></a><span data-ttu-id="0ab1b-170">C API �� XLM �Ƃ̊֌W</span><span class="sxs-lookup"><span data-stu-id="0ab1b-170">C API and Its Relation to XLM</span></span>

<span data-ttu-id="0ab1b-p119">Excel �}�N�� (XLM) ����́AExcel �Œ񋟂��ꂽ�A���[�U�[�����p�ł���ŏ��̃v���O���~���O���ł����B���[�U�[�́A�ʏ�̃��[�N�V�[�g�Ɏ��Ă�����ʂȃ}�N�� �V�[�g�ŁA�Ǝ��̃R�}���h��֐���쐬�ł��܂����BExcel 2013 �ł�A�������� XLM �}�N�� �V�[�g���T�|�[�g����Ă��܂��B **SUM** �� **LOG** �Ȃǂ̒ʏ�̃��[�N�V�[�g�֐����ׂĂ�}�N�� �V�[�g�Ŏg�p�ł��܂��B����Ƀ��[�N�V�[�g�ɓ��͂��邱�Ƃ͂ł��Ȃ����̍��ڂ�}�N�� �V�[�g�ł͎g�p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p119">The Excel macro (XLM) language was the first user-accessible programming environment provided in Excel. It enabled users to create custom commands and functions on special macro sheets that look like ordinary worksheets. XLM macro sheets are still supported in Excel 2013. You can use all the usual worksheet functions like **SUM** and **LOG** on a macro sheet, in addition to the following items that cannot be entered on a worksheet:</span></span> 
  
- <span data-ttu-id="0ab1b-175">���[�N�X�y�[�X���֐� ( **GET.CELL**�A **GET.WORKBOOK** �Ȃ�)�B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-175">Workspace information functions such as **GET.CELL** and **GET.WORKBOOK**.</span></span>
    
- <span data-ttu-id="0ab1b-176">�ʏ�̃��[�U�[����̎�������\�ɂ���A�R�}���h�Ɠ����̊֐� ( **DEFINE.NAME**�A **PASTE** �Ȃ�)�B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-176">Command-equivalent functions that enable automation of ordinary user operations such as **DEFINE.NAME** and **PASTE**.</span></span>
    
- <span data-ttu-id="0ab1b-177">�A�h�C���Ɋ֘A����֐� ( **REGISTER** �Ȃ�)�B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-177">Functions that relate to add-ins such as **REGISTER**.</span></span>
    
- <span data-ttu-id="0ab1b-178">�R�}���h�Ɠ����̃C�x���g �g���b�v ( **ON.ENRTY**�A **ON.TIME** �Ȃ�)�B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-178">Command-equivalent event traps such as **ON.ENRTY** and **ON.TIME**.</span></span>
    
- <span data-ttu-id="0ab1b-179">�}�N���֐��ŗL�̑��� ( **ARGUMENT**�A **VOLATILE** �Ȃ�)�B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-179">Macro function-specific operations such as **ARGUMENT** and **VOLATILE**.</span></span>
    
- <span data-ttu-id="0ab1b-180">�t���[���䑀�� ( **GOTO**�A **RETURN** �Ȃ�)�B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-180">Flow-control operations such as **GOTO** and **RETURN**.</span></span>
    
<span data-ttu-id="0ab1b-p120">Excel �o�[�W���� 3 �ɂ́AC API �̋@�\�����ł����݂��܂��B�������AExcel �o�[�W���� 4 �ł́AXLM ���ꂪ C API �Ƀ}�b�v����Ă��܂����B����ȍ~�ADLL �͂��ׂẴ��[�N�V�[�g�֐��A�}�N�� �V�[�g���֐��A�R�}���h�A�C�x���g �g���b�v�̐ݒ��Ăяo�����Ƃ��\�ɂȂ�܂����BDLL �́AC API ������� XLM �t���[����֐���Ăяo�����Ƃ͂ł��܂���B�����̃}�N�� �V�[�g�֐��ƃR�}���h�́A�w���v �t�@�C�� XLMacr8.hlp (�ȑO�� Macrofun.hlp �Ƃ������O�ł���) �ɋL�ڂ���Ă��܂��B���̃w���v �t�@�C������肷��ɂ́A�u[Microsoft �_�E�����[�h �Z���^�[](http://download.microsoft.com)�v�Ɉړ����A"XLMacr8.hlp" ��������܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p120">A limited version of the C API existed in Excel version 3. However, in Excel version 4, the XLM language was mapped to the C API. Since then, DLLs have been able to call all worksheet functions, macro sheet information functions, and commands, and to set event traps. DLLs cannot call XLM flow control functions from within the C API. These macro-sheet functions and commands are documented in the Help file XLMacr8.hlp (formerly named Macrofun.hlp). To obtain this help file, go to the [Microsoft Download Center](http://download.microsoft.com) and search for "XLMacr8.hlp".</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0ab1b-187">[!����] Windows Vista �� Windows 7 �́A���ڂɂ� .hlp �t�@�C����T�|�[�g���Ă��܂���B�������A���̃t�@�C����J�����Ƃ̂ł��� [Windows Vista �p�� Windows �w���v �v���O���� (WinHlp32.exe)]([](http://go.microsoft.com/fwlink/?LinkID=82148)�A[Windows 7 �p�� Windows �w���v �v���O���� (WinHlp32.exe)](http://www.microsoft.com/download/en/details.aspx?id=91) �� Microsoft ����_�E�����[�h�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-187">Windows Vista and Windows 7 do not directly support .hlp files, but you can download the [Windows Help program (WinHlp32.exe) for Windows Vista](http://go.microsoft.com/fwlink/?LinkID=82148) or the [Windows Help program (WinHlp32.exe) for Windows 7](http://www.microsoft.com/download/en/details.aspx?id=91) from Microsoft that enables them to be opened.</span></span> 
  
<span data-ttu-id="0ab1b-p121">DLL �́A�R�[���o�b�N�֐� **Excel4**�A **Excel4v**�A **Excel12**�A **Excel12v** (�Ō�� 2 �́AExcel 2007 �œ������ꂽ) ��g�p���āA�֐��ƃR�}���h�ɑΉ����� C API ��Ăяo���܂��B�e�֐��ƃR�}���h�ɑΉ�����񋓌^�̒萔�́A�w�b�_�[ �t�@�C���Œ�\`����A������ 1 �Ƃ��Ă����̃R�[���o�b�N�ɓn����܂��B���Ƃ��΁A **xlfGetCell** �ɑΉ����� **GET.CELL**�A **xlfRegister** �ɑΉ����� **REGISTER**�A **xlcDefineName** �ɑΉ����� **DEFINE.NAME** �ł��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p121">DLLs call C API equivalents of these functions and commands by using the callback functions **Excel4**, **Excel4v**, **Excel12**, and **Excel12v** (the last two were introduced in Excel 2007). Enumerated constants that correspond to each function and command are defined in a header file and passed as one of the arguments to these callbacks. For example, **GET.CELL** is represented by **xlfGetCell**, **REGISTER** by **xlfRegister**, and **DEFINE.NAME** by **xlcDefineName**.</span></span>
  
<span data-ttu-id="0ab1b-p122">���[�N�V�[�g�֐��A�}�N�� �V�[�g�֐��A�R�}���h��񋟂��邱�Ƃɉ����āAC API �� DLL ����炱���̃R�[���o�b�N��g�p���邱�Ƃɂ���Ă̂݌Ăяo�����Ƃ��ł���֐��ƃR�}���h�̗񋓑̂�񋟂��܂��B���Ƃ��΁A **xlGetName** �́ADLL �� Excel �Ɋ֐��ƃR�}���h��o�^����ꍇ�ɕK�v�Ƃ���ADLL ���̂̊��S�p�X�ƃt�@�C��������o�ł���悤�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p122">In addition to providing the worksheet functions and macro-sheet functions and commands, the C API provides function and command enumerations that can be called only by using these callbacks from within a DLL. For example, **xlGetName** enables the DLL to find out its own the full path and file name, which is required when you register functions and commands with Excel.</span></span> 
  
<span data-ttu-id="0ab1b-p123">Excel �o�[�W���� 5 �ł� Visual Basic for Applications (VBA) �V�[�g�̓����A�o�[�W���� 8 (Excel 97) �ł� Visual Basic Editor (VBE) �̓����ȍ~�A���[�U�[�� Excel ��J�X�^�}�C�Y����ł�e�Ղȕ��@�́AXLM �̑���� VBA ��g�p���邱�Ƃł��B���������āAExcel �̂���ȍ~�̃o�[�W�����œ������ꂽ�V�����@�\�̑����́AXLM �܂��� C API ���Ăł͂Ȃ� VBA ���ė��p�ł��܂��B���Ƃ��΁A�������̃R�}���h�A�C�x���g �g���b�v�A�g���_�C�A���O �{�b�N�X�@�\�́AXLM �܂��� C API ���Ăł͂Ȃ��AVBA ���ė��p�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-p123">Since the introduction of Visual Basic for Applications (VBA) sheets in Excel version 5, and the Visual Basic Editor (VBE) in version 8 (Excel 97), the easiest way for users to customize Excel is to use VBA instead of XLM. Consequently, much of the new functionality introduced in later versions of Excel is available through VBA, but not through XLM or the C API. For example, several commands, event traps, and enhanced dialog box capabilities are available through VBA, but not through XLM or the C API.</span></span>
  
<span data-ttu-id="0ab1b-196">�ڂ����́A�u[Excel �p C API �̐V�@�[](what-s-new-in-the-c-api-for-excel.md)(what-s-new-in-the-c-api-for-excel.md)�v��������������B</span><span class="sxs-lookup"><span data-stu-id="0ab1b-196">For more information, see [What's New in the C API for Excel](what-s-new-in-the-c-api-for-excel.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ab1b-197">�֘A����</span><span class="sxs-lookup"><span data-stu-id="0ab1b-197">See also</span></span>



<span data-ttu-id="0ab1b-198">[Excel �p C API �̐V�@�[](what-s-new-in-the-c-api-for-excel.md)(what-s-new-in-the-c-api-for-excel.md)</span><span class="sxs-lookup"><span data-stu-id="0ab1b-198">[What's New in the C API for Excel](what-s-new-in-the-c-api-for-excel.md)</span></span>
  
<span data-ttu-id="0ab1b-199">[C API �R�[���o�b�N�֐� Excel4�AExcel12](c-api-callback-functions-excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="0ab1b-199">[C API Callback Functions Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)</span></span>


[<span data-ttu-id="0ab1b-200">Excel XLL SDK �̊T�v</span><span class="sxs-lookup"><span data-stu-id="0ab1b-200">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)
