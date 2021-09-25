---
title: Excel での C API を使用したプログラミング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007],programming interfaces [Excel 2007],C API [Excel 2007], when to use,C API [Excel 2007], relation to XLM,Excel programming interfaces
ms.assetid: 142bc0ce-7d16-4b69-9799-ce6558da2def
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.localizationpriority: high
ms.openlocfilehash: f8ecad11c44dbe38e44c6160b75fd47a38bfbe9a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617161"
---
# <a name="programming-with-the-c-api-in-excel"></a>Excel での C API を使用したプログラミング

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 XLL �\�t�g�E�F�A�J���L�b�g�� C API ��g�p���āAExcel 2013 �̍��p�t�H�[�}���X�̃��[�N�V�[�g����쐬�ł��܂��BExcel 2013 �� C API �ւ̃A�b�v�O���[�h�́A�T�[�h �p�[�e�B���@�\�܂��͓���@�\�̃p�t�H�[�}���X���d�v�ȈӖ�������[�U�[�ɑ��Čp�����čs���Ă���T�|�[�g�𔽉f���܂��B
  
## <a name="excel-programming-interfaces"></a>Excel のプログラミング インターフェイス

Excel には、インターフェイスを使用して Excel と接続するアプリケーションを開発するためのいくつかのオプションが用意されています。Excel のプログラミング インターフェイスは、次の順序で以前のバージョンに追加されました。
  
- **XLM �}�N������:** Excel �̊g���@�\�̂��߂Ƀ��[�U�[���g�p�ł���ŏ��̌���ŁAC API �̊�b�ɂȂ�܂����BXLM �́AExcel 2010 �ł�T�|�[�g����Ă��܂������A���Ȃ�ȑO�� Visual Basic for Applications (VBA) �ɒu���������܂����B 
    
- **C API �� XLL:** Excel �ɓ�������Ă��� DLL �ł��B������ DLL �́A���p�t�H�[�}���X�̃��[�N�V�[�g����ǉ�����ł���ړI�ōő��̃C���^�[�t�F�C�X��񋟂��܂��B�������A����ȍ~�̋Z�p�Ɣ�r���Ă����炩���G�ł��B 
    
- **VBA:** Excel �u�b�N �I�u�W�F�N�g�Ɋ֘A�t�����Ă��� Visual Basic �R�[�h �I�u�W�F�N�g�ł��BVBA �́A�C�x���g �g���b�v�A�J�X�^�}�C�Y�A���[�U�[��`���ƃR�}���h�̒ǉ���\�ɂ��Ă��܂��BVBA �́A�ł��ʓI�Ɏg�p����A�ł�e�Ղɗ��p�ł���g���I�v�V�����ł��B 
    
- **COM:** Windows �x�[�X�̃A�v���P�[�V���������̑��݉^�p���̕W���ł��BExcel �́A������ăC�x���g��I�u�W�F�N�g����J���܂��BVBA �́ACOM ��g�p���� Excel �ƑΘb���܂��BExcel �́A�O������ Excel �𐧌䂷�� C++ COM �R�[�h�̃��\�[�X��A�v���P�[�V������쐬����̂ɖ𗧂� COM �^�C�v ���C�u������G�N�X�|�[�g���܂��B 
    
- **Microsoft .NET Framework:** ���U���̐v���ȃA�v���P�[�V�����J���p�ɐv���ꂽ�A��������}�l�[�W �R�[�h���ł��B.NET Framework �����̃R�[�h�̎�v�ȃv���O���~���O����� C# �ł����A�����̌���� Microsoft ���Ԍ��� (MSIL) �ɃR���p�C���ł��܂��BExcel 2013 �ł�, .NET Framework �A�Z���u���Ɋ܂܂��R�[�h ���\�[�X�ɃA�N�Z�X�ł��܂��B 
    
## <a name="when-to-use-the-c-api"></a>C API を使用する場合

The primary reason for writing XLLs and using the C API is to create high-performance worksheet functions. Although XLL functions are frequently referred to as user-defined functions, the investment in time to obtain the understanding and skills that are required to write XLLs make this a technology impractical for most users. Nevertheless, the applications of high-performance functions—and, in Excel 2013, the ability to write multithreaded interfaces to powerful server resources—make this a very important part of Excel extensibility. 
  
Excel 2007 で導入された C API の改訂は、ユーザー インターフェイスなどの機能ではなく、主に高性能な計算に関連する側面に関係しています。
  
### <a name="writing-high-performance-user-defined-worksheet-functions"></a>高パフォーマンスのユーザー定義ワークシート関数の作成

XLL �A�h�C����쐬���āA���p�t�H�[�}���X�̃��[�N�V�[�g����쐬����ꍇ�AExcel �� C API �͗��z�I�ȑI����ł��BC API ��g�p����ƁA���[�N�V�[�g�̃f�[�^�֍ł���ړI�ɃA�N�Z�X�ł��܂��BXLL ��g�p����ƁAExcel �� DLL ���\�[�X�֍ł���ړI�ɃA�N�Z�X�ł���悤�ɂȂ�܂��BExcel 2013 �ł́A�V�����f�[�^�^���ǉ�����邱�Ƃɂ���āA�܂��ł�d�v�Ȃ��ƂƂ��āA�N���X�^�[�����ꂽ�T�[�o�[�ł̃��[�U�[��`���̎��s���T�|�[�g����邱�Ƃɂ���āAXLL �̃p�t�H�[�}���X�͂���Ɍ��サ�Ă��܂��B
  
XLL の使用にはコストがかかります。C API には、VBA、COM、.NET Framework にある、かなり高レベルの迅速な開発機能はありません。メモリ管理は低レベルで行われるので、開発者により大きな責任を負わせることになります。COM 経由で公開されている多くの Excel 機能は、VBA と.NET Framework を介して利用できますが、C API には公開されていません。
  
### <a name="accessing-multithreaded-servers-by-using-xll-worksheet-functions"></a>XLL ワークシート関数を使用したマルチスレッド サーバーへのアクセス

Excel 2007 で導入された、マルチ スレッド再計算 (MTR) を使用すると、スレッド セーフな XLL ワークシート関数を作成できます。マルチ スレッド サーバーにアクセスするのに、これらの関数を使用できます。以下のセクションでは、ユーザーが観察するパフォーマンスをどのように大幅に向上させることができるかを詳細に説明します。処理能力を大量に消費する必要がある Excel ユーザーに対して、MTR を使用する XLL と強力な計算サーバーの組み合わせは、最高のパフォーマンス ソリューションを提供します。
  
### <a name="customizing-the-excel-user-interface"></a>Excel ユーザー インターフェイスのカスタマイズ

Excel の多くのバージョンでは、C API はユーザー インターフェイスをカスタマイズする際に、最適な選択肢ではありませんでした。VBA は、Excel のオブジェクトとイベントへのアクセスに優れています。Excel 2007 で導入されたユーザー インターフェイスは、外観と基本技術の両面で、以前のバージョンとは大きく異なります。マネージ コードのリソースを使用して、このインターフェイスを最適にカスタマイズできます。
  
### <a name="creating-applications-that-can-be-accessed-on-the-internet"></a>インターネット上でアクセス可能なアプリケーションの作成

2007 Microsoft Office system で導入された Excel Services では、標準の Web ブラウザー ツールを使用して、ユーザーがブックと Excel の機能にアクセスする最善の方法を提供します。.NET Framework 開発言語とリソースと共に、これらの技術は将来に渡ってユーザーにとって Excel 展開の重要な部分になります。
  
### <a name="controlling-excel-from-external-applications"></a>外部アプリケーションからの Excel の制御

Excel は、そのオブジェクト、メソッド、イベントを COM インターフェイス経由で公開します。したがって、Excel セッションを開始して制御したり、既存の Excel セッションを制御したりするスタンドアロン アプリケーションを作成するために COM を使用できます。C++ と VBA を含む、いくつかの開発言語で COM に公開されている Excel インターフェイスにアクセスできます。C# と .NET Framework では、同様に Excel へのリモート アクセスと制御を可能にする Excel へのインターフェイスを提供します。
  
## <a name="asynchronous-calling-of-excel"></a>Excel の非同期呼び出し

Excel は XLL に制御をすでに渡している場合にのみ、XLL が C API を呼び出すことができるようにします。Excel が呼び出すワークシート関数は、C API を使用して Excel にコールバックできます。Excel が呼び出す XLL コマンドは、C API を呼び出すことができます。VBA それ自体が Excel によって呼び出されるときに VBA が呼び出す DLL、XLL 関数、コマンドは、C API を呼び出すことができます。たとえば、時間指定の Windows コールバックを XLL に設定し、その XLL から C API を呼び出すことはできません。また、XLL によって作成されたバック グラウンド スレッドから C API を呼び出すこともできません。DLL または XLL から COM を使用して非同期に Excel を呼び出すことはお勧めできません。
  
イベントに非同期に応答する Excel のアプリケーションがある場合、これには多くの制限があります。たとえば、Excel がインターネット上のデータの一部を取得し、データが変更されるたびに再計算するようにしたいとします。あるいは、バックグラウンド スレッドで計算を実行し、その終了時に Excel が再計算するようにしたい場合もあります。
  
Excel が変更をアクティブにポーリングするようにすれば実現できますが、これは Excel が頻繁に通常の処理を中断するので効率的ではありませんし、制限があります。理想的なソリューションではありませんが、C API または VBA を使用して、時間指定で繰り返すコマンドを設定することもできます。
  
理想的には、データの変更を検出し、Excel をトリガーして更新の取得と再計算を実行させる、より効率的な外部プロセスが望まれます。COM を使用して Excel とインターフェイスを介して接続するアプリケーションを使用することによって、これを実現できます。Excel が明示的に制御を渡す場合にのみ呼び出す C API と同じような制限は COM にはありません。ダイアログボックスが表示されていたり、メニューがプルダウンされていたり、マクロが実行されている場合は、メソッドの呼び出しは無視されます。しかし、Excel が準備完了状態のときにはいつでも、COM アプリケーションは Excel メソッドを呼び出すことができます。
  
## <a name="c-api-and-its-relation-to-xlm"></a>C API と XLM との関係

Excel �}�N�� (XLM) ����́AExcel �Œ񋟂��ꂽ�A���[�U�[�����p�ł���ŏ��̃v���O���~���O���ł����B���[�U�[�́A�ʏ�̃��[�N�V�[�g�Ɏ��Ă�����ʂȃ}�N�� �V�[�g�ŁA�Ǝ��̃R�}���h�����쐬�ł��܂����BExcel 2013 �ł�A�������� XLM �}�N�� �V�[�g���T�|�[�g����Ă��܂��B **SUM** �� **LOG** �Ȃǂ̒ʏ�̃��[�N�V�[�g�����ׂĂ�}�N�� �V�[�g�Ŏg�p�ł��܂��B����Ƀ��[�N�V�[�g�ɓ��͂��邱�Ƃ͂ł��Ȃ����̍��ڂ�}�N�� �V�[�g�ł͎g�p�ł��܂��B 
  
- ���[�N�X�y�[�X���� ( **GET.CELL**�A **GET.WORKBOOK** �Ȃ�)�B
    
- �ʏ�̃��[�U�[����̎�������\�ɂ���A�R�}���h�Ɠ����̊� ( **DEFINE.NAME**�A **PASTE** �Ȃ�)�B
    
- �A�h�C���Ɋ֘A����� ( **REGISTER** �Ȃ�)�B
    
- �R�}���h�Ɠ����̃C�x���g �g���b�v ( **ON.ENRTY**�A **ON.TIME** �Ȃ�)�B
    
- �}�N�����ŗL�̑��� ( **ARGUMENT**�A **VOLATILE** �Ȃ�)�B
    
- �t���[���䑀�� ( **GOTO**�A **RETURN** �Ȃ�)�B
    
Excel �o�[�W���� 3 �ɂ́AC API �̋@�\�����ł����݂��܂��B�������AExcel �o�[�W���� 4 �ł́AXLM ���ꂪ C API �Ƀ}�b�v����Ă��܂����B����ȍ~�ADLL �͂��ׂẴ��[�N�V�[�g���A�}�N�� �V�[�g�����A�R�}���h�A�C�x���g �g���b�v�̐ݒ��Ăяo�����Ƃ��\�ɂȂ�܂����BDLL �́AC API ������� XLM �t���[�������Ăяo�����Ƃ͂ł��܂���B�����̃}�N�� �V�[�g���ƃR�}���h�́A�w���v �t�@�C�� XLMacr8.hlp (�ȑO�� Macrofun.hlp �Ƃ������O�ł���) �ɋL�ڂ���Ă��܂��B���̃w���v �t�@�C������肷��ɂ́A�u[Microsoft �_�E�����[�h �Z���^�[](https://download.microsoft.com)�v�Ɉړ����A"XLMacr8.hlp" ��������܂��B 
  
> [!NOTE]
> [!����] Windows Vista �� Windows 7 �́A���ڂɂ� .hlp �t�@�C����T�|�[�g���Ă��܂���B�������A���̃t�@�C����J�����Ƃ̂ł��� [Windows Vista �p�� Windows �w���v �v���O���� (WinHlp32.exe)]([](https://go.microsoft.com/fwlink/?LinkID=82148)�A[Windows 7 �p�� Windows �w���v �v���O���� (WinHlp32.exe)](https://www.microsoft.com/download/en/details.aspx?id=91) �� Microsoft ����_�E�����[�h�ł��܂��B 
  
DLL �́A�R�[���o�b�N�� **Excel4**�A **Excel4v**�A **Excel12**�A **Excel12v** (�Ō�� 2 �́AExcel 2007 �œ������ꂽ) ��g�p���āA���ƃR�}���h�ɑΉ����� C API ��Ăяo���܂��B�e���ƃR�}���h�ɑΉ�����񋓌^�̒萔�́A�w�b�_�[ �t�@�C���Œ�`����A������ 1 �Ƃ��Ă����̃R�[���o�b�N�ɓn����܂��B���Ƃ��A **xlfGetCell** �ɑΉ����� **GET.CELL**�A **xlfRegister** �ɑΉ����� **REGISTER**�A **xlcDefineName** �ɑΉ����� **DEFINE.NAME** �ł��B
  
���[�N�V�[�g���A�}�N�� �V�[�g���A�R�}���h��񋟂��邱�Ƃɉ����āAC API �� DLL ����炱���̃R�[���o�b�N��g�p���邱�Ƃɂ���Ă̂Ăяo�����Ƃ��ł�����ƃR�}���h�̗񋓑̂�񋟂��܂��B���Ƃ��A **xlGetName** �́ADLL �� Excel �Ɋ��ƃR�}���h��o�^����ꍇ�ɕK�v�Ƃ���ADLL ���̂̊��S�p�X�ƃt�@�C��������o�ł���悤�ɂ��܂��B 
  
Excel バージョン 5 での Visual Basic for Applications (VBA) シートの導入、バージョン 8 (Excel 97) での Visual Basic Editor (VBE) の導入以降、ユーザーが Excel をカスタマイズする最も容易な方法は、XLM の代わりに VBA を使用することです。したがって、Excel のそれ以降のバージョンで導入された新しい機能の多くは、XLM または C API を介してではなく VBA を介して利用できます。たとえば、いくつかのコマンド、イベント トラップ、拡張ダイアログ ボックス機能は、XLM または C API を介してではなく、VBA を介して利用できます。
  
�ڂ����́A�u[Excel �p C API �̐V�@�[](what-s-new-in-the-c-api-for-excel.md)(what-s-new-in-the-c-api-for-excel.md)�v��������������B
  
## <a name="see-also"></a>関連項目



[Excel 用 C API の新機能](what-s-new-in-the-c-api-for-excel.md)
  
[C API コールバック関数 Excel4、Excel12](c-api-callback-functions-excel4-excel12.md)


[Excel XLL SDK の概要](getting-started-with-the-excel-xll-sdk.md)

