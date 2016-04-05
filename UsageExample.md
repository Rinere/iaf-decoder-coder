# Class usage example #

```

require_once 'File_Format_Iaf.php';

$iaf = new File_Format_Iaf();

// если нужно, то загружаем из файла
// if (!$iaf->load('mail.iaf')) echo 'error=' . $iaf->error();


$iaf->AccountName = 'Почтовый ящик me@example.ru';
$iaf->MakeAvailableOffline = 1;

// pop3 настройки

$iaf->POP3Server = 'pop3.example.ru';
$iaf->POP3UserName = 'me';
$iaf->POP3Password = 'sfd7Dg24';
$iaf->POP3Port = 995;
$iaf->POP3SecureConnection = 1;
$iaf->POP3LeaveMailOnServer = 0;
$iaf->POP3PasswordPrompt = 0;

// smtp

$iaf->SMTPDisplayName = 'Фамилия Имя';
$iaf->SMTPEmailAddress = 'me@example.ru';
$iaf->SMTPServer = 'smtp.example.ru';
$iaf->SMTPUserName = 'me';
$iaf->SMTPPassword = 'HJGhgsdf';
$iaf->SMTPPasswordPrompt = 0;
$iaf->SMTPPort = 25;
$iaf->SMTPSecureConnection = 1;
$iaf->SMTPAuthMethod = 3;


// get all values
// $iaf->getFields();

// get value
// echo 'POP3Password = ' . $iaf->POP3Password;

// save to new file
// $iaf->save('new.iaf');

// save to input file
//$iaf->save();

// output to browser
// $iaf->render();


```