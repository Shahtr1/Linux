OBJDIR := objdir
OBJS := $(addprefix $(OBJDIR)/,foo.o bar.o baz.o)

$(OBJDIR)/%.o : %.c
	$(COMPILE.c) $(OUTPUT_OPTION) $<

all: $(OBJS)

print: *.c
	lpr -p $?
	touch print 	

$(OBJS): | $(OBJDIR)

$(OBJDIR):
	mkdir $(OBJDIR)
	
