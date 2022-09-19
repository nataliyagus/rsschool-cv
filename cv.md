# Nataliya Gusakova

## Contacts

- phone: +48 576 595 772
- Viber: +375 29 781 22 34
- Email: natali.liliya85@gmail.com

## Tech Skills

- HTML5
- CSS
- GIT
- SQL
- Pascal (Delphi)
- C++
- FoxPro
- VisualBasic

## Work Experience

### Grodno Stade Medical University

programmer

feb 2011 - jan 2020

## Education

### Belarusian National Technical University

_International Institute for Distance Education_

_Information technology software_

programmer

September 2005 - June 2010

## About myself

I started interested in programming at school, it was when I began studying Paskal.
I continued my studies in college. After it at BNTU's Department of Information Systems and Technologies.
When I graduated from the university, I started my first job at GrSMU as a programmer in the Information technology department.
 Over the years of working in this position, I gained experience with accounting, training and personnel management programs. I was involved in updating the process of teaching students and managing their daily routine: a distance learning portal (edu.grsmu.by), an electronic library card and a pass system based on student cards. 
Every time when I got acquainted with new technologies and introduce them to the university's everyday life, I discovered a lot of new things, every day I learned and developed something new.
I've always been passionate about learning and using all this knowledge in practice. So it's time to learn something new, something really useful nowadays and I've decided to start learning Javascript. Because so far it was a very practical and useful tool and looks like it will be in the nearest future.
After overviewing various schools and their curriculum, my choice fell on RS School. I'll be glad to become one of your students.

## Code Examples

procedure TForm1.Button1Click(Sender: TObject);

var

s,c,s1 :string ;

ch1,ch2:char;

n,i:integer;

begin


 Edit1.Text:=Clipboard.AsText;

 s:=Clipboard.AsText;

 if s<>'' then begin

 ch1:=s[1];

 ch2:=s[2];

 Label1.Caption:=ch1+ch2;

 if (ch1='F') and (ch2='F') then

   begin

    n:=HexToDec(s);

    Edit2.Text:=IntToStr(n);


    Data.DataModule1.ADOQuery1.Close;

     data.DataModule1.ADOQuery1.SQL.Text:='select c.idchip, 
     
     b.nomz from ez_cards c, photos ph, cards_student_v b '+ 
     
      'where ph.idperson=b.rowguid and ph.idphotos = c.idphotos
      
       and c.encodedate is not null'+  ' and c.idchip='+chr(39)
       
       +Edit2.Text+chr(39) ;

     data.DataModule1.ADOQuery1.open;

     if data.DataModule1.ADOQuery1.FieldValues['nomz']>'' then

        c:=data.DataModule1.ADOQuery1.FieldValues['nomz']
    else 

     begin
            Data.DataModule1.ADOQuery1.Close;

            data.DataModule1.ADOQuery1.SQL.Text:='select 
            
            c.idchip, b.nomz from ez_cards c, photos ph, 
            
            CARDS_SOTR_V b '+ 'where ph.idperson=b.rowguid and 
            
            ph.idphotos = c.idphotos and c.encodedate is not 
            
            null'+ ' and c.idchip='+chr(39)+Edit2.Text+chr(39) ;

            data.DataModule1.ADOQuery1.open;

            if data.DataModule1.ADOQuery1.FieldValues['nomz']>0 then

                c:=data.DataModule1.ADOQuery1.FieldValues['nomz'];
        end;
 
    s1:='';

    for i:=1 to Length(c) do

        if c[i]<>' ' then s1:=s1+c[i];

    if c>'' then Label2.Caption:=s1;
   
    Clipboard.AsText:=Label2.Caption ;

    Timer2.Enabled:=true;

    end;                
 end;

## Languages
* Russian
* English
* Polish