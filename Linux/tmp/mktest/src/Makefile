PROGS   = foo
OBJECTS = foo.o bar.o

# Shouldn't need to change anything below here...

OBJDIR = ../obj

VPATH = $(OBJDIR)

$(OBJDIR)/%.o : %.c
	$(COMPILE.c) $< -o $@

OBJPROG = $(addprefix $(OBJDIR)/, $(PROGS))

all: $(OBJPROG)

$(OBJPROG): $(addprefix $(OBJDIR)/, $(OBJECTS))
	$(LINK.o) $^ $(LDLIBS) -o $@